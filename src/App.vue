<template>
  <div id="app">
    <h1>Todo application</h1>
    <TodoList v-bind:todos="todos" />
  </div>
</template>

<script>
import TodoList from "@/components/TodoList.vue";
export default {
  name: "App",
  data() {
    return {
      todos: [
        { id: 1, title: "Buy bread", compleated: false },
        { id: 2, title: "Buy butter", compleated: false },
        { id: 3, title: "Buy coca-cola", compleated: false },
      ],
    };
  },
  components: {
    TodoList,
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
