<template>
  <div>
    <ul>
      <h4 v-if="encabezado">{{ encabezado }}</h4>
      <li v-for="(lista, i) in listas" :lista="lista" :key="i"> <a :href="lista.url"> {{ lista.texto }} </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MiLista",
  props: {
    encabezado: String,
    listas: Array
  }
};
</script>

<style scoped>
li {
  text-align: left;
  list-style: none;
}
h4 {
  text-align: left;
}
a {
  text-decoration: none;
  color: #9efdba;
}
</style>