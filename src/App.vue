<template>
  <div>
    Hi,{{ name_first }}.
    <navigation-link url="https://github.com/GagaSissi/just-practice-vue">
      <template v-slot:image>
        <img
          src="https://d10s7cl4nxfjv3.cloudfront.net/wp-content/uploads/sites/2/2019/09/vuejs-schulung-inhouse-logo.png"
        />
      </template>
      >Zum Profil</navigation-link
    >
    <TodoList />
  </div>
</template>

<script>
import TodoList from "./components/TodoList";
import NavigationLink from "./components/NavigationLink";
export default {
  name: "App",
  data: () => ({
    name_first: "Cecilia",
  }),
  components: {
    TodoList,
    NavigationLink,
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
img {
  height: 20px;
}

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
