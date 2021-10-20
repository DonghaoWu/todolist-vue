<template>
  <div class="title">
    <p>Completed Tasks:{{ todos.filter(todo => todo.done === true).length }}</p>
    <p>
      Completed Tasks:{{ todos.filter(todo => todo.done === false).length }}
    </p>
    <todo
      v-for="todo in todos"
      v-on:delete-todo="deleteTodo"
      v-on:complete-todo="completeTodo"
      :todo="todo"
      :key="todo.id"
    ></todo>
  </div>
</template>

<script>
import Todo from './Todo.vue';

export default {
  components: {
    Todo,
  },
  props: ['todos'],
  methods: {
    deleteTodo(todo) {
      const todoIndex = this.todos.indexOf(todo);
      this.todos.splice(todoIndex, 1);
    },
    completeTodo(todo) {
      const todoIndex = this.todos.indexOf(todo);
      this.todos[todoIndex].done = !this.todos[todoIndex].done;
    },
  },
};
</script>

<style>
.title {
  display: flex;
  flex-direction: column;

  align-items: center;
}
</style>
