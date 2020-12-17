<template>
  <div id="app" class="w-2/4 mx-auto">
    <DoubleRange />
  </div>
</template>

<script>
import DoubleRange from "./components/DoubleRange.vue";


export default {
  name: "App",
  components: {
    DoubleRange
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
