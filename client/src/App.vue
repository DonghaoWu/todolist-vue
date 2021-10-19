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
  methods: {
    addTodo(content) {
      this.todos.push(content);
    },
  },

  data() {
    return {
      todos: [
        {
          id: '001',
          title: 'Todo A',
          project: 'Project A',
          done: false,
        },
        {
          id: '002',
          title: 'Todo B',
          project: 'Project B',
          done: true,
        },
        {
          id: '003',
          title: 'Todo C',
          project: 'Project C',
          done: false,
        },
        {
          id: '004',
          title: 'Todo D',
          project: 'Project D',
          done: false,
        },
      ],
    };
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
