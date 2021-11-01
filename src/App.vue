<template>
  <div>
    <strong>{{ name_first }}</strong
    >,
    {{ age + " " + gender + "," }}
    {{ name_last }}
    <hr />
    {{ fullName }}
    <hr />
    {{ `${name_first} ${name_last}, ist ${age} Jahre jung.` }}
    <hr />
    {{ age >= 18 ? "volljährig" : "nicht volljärig" }}
  </div>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    name_first: "Cecilia",
    name_last: "Strüber",
    age: 38,
    gender: "female",
  }),
  computed: {
    fullName() {
      return this.name_first + " " + this.name_last;
    },
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
