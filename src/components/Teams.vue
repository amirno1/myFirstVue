<template>
  <div class="hello">
    <div v-bind:key="team.id" v-for="team in teams ">
      <h2>{{team.name}}</h2>
      <Information v-bind:information="information" v-bind:team="team" />
    </div>
  </div>
</template>

<script>
import Information from "./Information";
export default {
  name: "Teams",
  props: {
    teams: Array
  },
  data() {
    return {
      information: [
        { id: 1, name: "Perspolis", color: "Red" },
        { id: 2, name: "Esteghlal", color: "Blue" },
        { id: 3, name: "Sepahan", color: "Yellow" }
      ]
    };
  },
  components: {
    Information
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
