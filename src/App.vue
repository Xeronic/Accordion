<template>
  <div id="app">
    <img src="./assets/logo.png">
    <Accordion title="Press me to uncollapse">
      <template slot="Body">
      <h3>Something fun!</h3>
      <p>Hi all, something fun is up tonight!</p>
      </template>
    </Accordion>
  </div>
</template>

<script>
import Accordion from "./components/Accordion.vue";

export default {
  name: "app",
  components: {
    Accordion
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
