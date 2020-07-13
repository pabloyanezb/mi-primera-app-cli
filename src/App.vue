<template>
  <div id="app" class="background">
    <div class="container">
      <h2>
        Conocimientos de
        <b>{{ nombre }}</b>
      </h2>
      <MiLista encabezado="Aprendidos" :listas="aprendidos" />
      <MiLista encabezado="Por Aprender" :listas="aprender" />
    </div>
  </div>
</template>

<script>
import MiLista from "./components/MiLista.vue";

export default {
  name: "App",
  components: {
    MiLista
  },
  data: () => {
    return {
      nombre: "Pablo",
      aprendidos: [
        { texto:"HTML", url:"https://developer.mozilla.org/es/docs/Web/HTML"},
        { texto:"CSS", url:"https://developer.mozilla.org/es/docs/Web/CSS"},
        { texto:"JavasScript", url:"https://www.javascript.com"},
        { texto:"JQuery", url:"https://jquery.com"},
        { texto:"ES6", url:"https://www.w3schools.com/js/js_es6.asp"},
      ],
      aprender: [
        { texto:"Vue", url:"https://vuejs.org"},
        { texto:"React", url:"https://es.reactjs.org"}
      ]
    };
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
.background {
  position: absolute;
  height: 100%;
  width: 100%;
  background: #348f50;
  background: linear-gradient(to right, #56b4d3, #348f50);
}
.container {
  background-color: rgba(53, 53, 53, 0.102);
  border-radius: 10px;
  padding: 25px;
  margin-top: 3rem;
  backdrop-filter: blur(5px);
  box-shadow: -7px -7px 23px -4px rgba(0, 0, 0, 0.2);
  max-width: 280px;
  position: absolute;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
  color: #e8f9ff;
}
h2 {
  margin-bottom: 2rem;
  text-align: center;
}
</style>
