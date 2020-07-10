<template>
  <div class="background">
    <div class="container">
      <h2>
        Conocimientos de
        <b>{{ name }}</b>
      </h2>
      <ul>
        <h4 v-if="encabezado">Aprendidos</h4>
        <li v-for="(unItem, i) in Aprendidos" v-bind:key="i">{{ unItem }}</li>
      </ul>
      <ul>
        <h4 v-if="encabezado">Por aprender</h4>
        <li v-for="(unItem, i) in Estudiar" v-bind:key="i">
          <span v-if="i%2==0">{{++i}}.{{ unItem }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "MiLista",
  data: function() {
    return {
      name: "Pablo",
      encabezado: true,
      Aprendidos: ["HTML", "CSS", "Javascript", "JQuery", "ES6"],
      Estudiar: ["Vue", "Python", "React", "Angular"]
    };
  }
};
</script>

<style scoped>
.background {
  position: absolute;
  height: 100%;
  width: 100%;
  background: #348f50; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #56b4d3,
    #348f50
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #56b4d3,
    #348f50
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
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
li {
  text-align: left;
  list-style: none;
}
h2 {
  margin-bottom: 2rem;
}
h4 {
  text-align: left;
}
</style>