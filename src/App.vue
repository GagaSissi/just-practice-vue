<template>
  <div>
    Hi,{{ name_first }}.
    <input type="text" name="abc" value="xyz" @keyup="test2" />
    <a href="?seite=23" @click.right.prevent="test">Gehe zu Seite 23</a>
    <!-- .page-down
    .enter
    .tab
    .delete
    .esc
    .space

    .ctrl
    .alt
    .shift
    .meta.exact

@keyup.alt.67 

event modifier-->

    <TodoList />
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
  methods: {
    test() {
      alert("heyho lets go");
    },
    test2() {
      alert("adios");
    },
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
