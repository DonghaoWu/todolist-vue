<template>
  <div>
    <div id="app"></div>
    <my-todo-list v-bind:todos="todos"></my-todo-list>
    <create-todo v-on:add-todo="addTodo"></create-todo>
  </div>
</template>

<script>
import MyTodoList from './components/MyTodoList.vue';
import CreateTodo from './components/CreateTodo.vue';

export default {
  name: 'App',
  components: {
    MyTodoList,
    CreateTodo,
  },
  data() {
    return {
      todos: [],
    };
  },
  mounted() {
    this.fetchData();
  },
  methods: {
    addTodo(newTodo) {
      this.todos.push(newTodo);
    },
    async fetchData() {
      const res = await fetch('data.json');
      const data = await res.json();
      this.todos = data;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
