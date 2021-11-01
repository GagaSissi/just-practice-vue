<template>
  <div>
    Hi,{{ name_first }}.
    <ul>
      <li>Berlin</li>
      <li>Hamburg</li>
      <li>Frankfurt</li>
    </ul>
    <ul>
      <li v-for="(city, index) in cities" v-bind:key="city.id">
        {{ ++index }}. {{ city.name }}
      </li>
    </ul>
    <p v-for="n in 10" v-bind:key="n">{{ n }}</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    name_first: "Cecilia",
    cities: [
      { id: 1, name: "Berlin" },
      { id: 2, name: "Hamburg" },
      { id: 3, name: "Frankfurt" },
    ],
  }),
  computed: {
    fullName() {
      return this.name_first + " " + this.name_last;
    },
  },
};
</script>

<style>
.age {
  border: 1px solid red;
  margin: 5px;
  padding: 10px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
