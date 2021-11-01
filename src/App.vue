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
    <div class="age">
      {{ age }}.
      <span v-if="age < 18">Du bist unter 18.</span>
      <span v-else-if="age == 18">Super, du bist volljährig</span>
      <span v-else>Über 18 Jahre.</span>
    </div>
    <!-- Rendering bei v-show nur am Anfang der Seite. -->
    <!-- <div v-show="name_first == 'Cecilia'"></div> -->
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
