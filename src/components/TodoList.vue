<template>
  <ul>
    <TodoListItems
      v-for="todo in todos"
      :key="todo.id"
      :item="todo"
      @toggle="toggleListItem"
    />
  </ul>
</template>

<script>
import TodoListItems from "./TodoListItems";
export default {
  data: () => ({
    todos: [
      { id: 1, finished: false, name: "Vue JS lernen" },
      { id: 2, finished: false, name: "Schwarze Tonne rein holen" },
      { id: 3, finished: false, name: "Staubsauger starten" },
      { id: 4, finished: true, name: "Büro umbauen" },
    ],
  }),
  name: "TodoList",
  components: {
    TodoListItems,
  },
  methods: {
    toggleListItem(el) {
      el.finished = !el.finished;
    },
  },
};
</script>

<style></style>
