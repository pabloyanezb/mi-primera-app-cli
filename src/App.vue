<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <MiLista></MiLista>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import MiLista from "./components/MiLista.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    MiLista
  }
};
</script>

<style>
body {
  margin: 0 !important;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
