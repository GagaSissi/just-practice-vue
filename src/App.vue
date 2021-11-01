<template>
  <div>
    Hi,{{ name_first }}.
    <ul>
      <li
        v-for="(todo, index) in todos"
        :key="todo.id"
        :class="{ finishedTask: todo.finished }"
      >
        <input type="checkbox" :checked="todo.finished" />

        <a href="'?id='+todo.id">show</a> {{ ++index }}. {{ todo.name }}
      </li>
    </ul>
    <button @click="test">Test</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    name_first: "Cecilia",
    todos: [
      { id: 1, finished: false, name: "Vue JS lernen" },
      { id: 2, finished: false, name: "Schwarze Tonne rein holen" },
      { id: 3, finished: false, name: "Staubsauger starten" },
      { id: 4, finished: true, name: "Büro umbauen" },
    ],
  }),
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
