<template>
  <div>
    <p>Completed Tasks:{{ todos.filter(todo => todo.done === true).length }}</p>
    <p>
      Completed Tasks:{{ todos.filter(todo => todo.done === false).length }}
    </p>
    <todo v-for="todo in todos" :todo="todo" :key="todo.id"></todo>
  </div>
</template>

<script>
import Todo from './Todo.vue';

export default {
  components: {
    Todo,
  },
  props: ['todos'],
};
</script>

<style></style>
