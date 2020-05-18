<template>
  <div>
    <div v-bind:key="info.id" v-for="info in information">
      <div v-bind:class="info.color.toLowerCase()" v-if="info.id === team.id">{{info.color}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "information",
  props: {
    information: Array,
    team: Object
  }
};
</script>

<style scoped>
.red {
  color: red;
}
.blue {
  color: blue;
}
.yellow {
  color: yellow;
}
</style>

