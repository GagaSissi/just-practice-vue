<template>
  <div>
    Hi,{{ name_first }}.
    <TodoList />
    <button @click="test">Test</button>
  </div>
</template>

<script>
import TodoList from "./components/TodoList";
export default {
  name: "App",
  data: () => ({
    name_first: "Cecilia",
  }),
  components: {
    TodoList,
  },
};
</script>

<style>
.finishedTask {
  text-decoration: line-through;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
