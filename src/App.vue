<template>
  <div id="app">
    <Teams v-bind:teams="teams" />
  </div>
</template>

<script>
import Teams from "./components/Teams.vue";

export default {
  name: "App",
  data() {
    return {
      teams: [
        { id: 1, name: "Perspolis", title: "Champion" },
        { id: 2, name: "Esteghlal", title: "Loser" },
        { id: 3, name: "Sepahan", title: "Not applicable" }
      ]
    };
  },
  components: {
    Teams
  }
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
