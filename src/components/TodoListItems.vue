<template>
  <li :class="{ finishedTask: item.finished }">
    <input type="checkbox" :checked="item.finished" />
    <button @click="toggleItem">toggle</button>
    {{ item.name }}
  </li>
</template>

<script>
export default {
  name: "TodoListItems",
  props: ["item"],
  methods: {
    toggleItem() {
      this.$emit("toggle", this.item);
    },
  },
};
</script>
