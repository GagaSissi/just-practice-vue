<template>
  <a :href="url" class="nav-link">
    <slot name="image"></slot> |
    <slot></slot>
  </a>
</template>

<script>
export default {
  props: ["url"],
  name: "NavigationLink",
};
</script>

<style>
a:link,
a:active,
a:visited,
a:hover {
  color: red;
}
</style>
