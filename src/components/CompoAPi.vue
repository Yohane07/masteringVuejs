<template>
  <h1>Composition API</h1>
  <p>La composition API en gros évite d'avoir toute cette structure avec data, method, computed, watcher etc </p>

  <p>Il va me permettre par exemple d'avoir des variables réactives et les manipuler
  directement sans passer par une fonction qui se trouve dans method. Par exemple</p>

  <h3>{{compteurGame}}</h3>
  <button @click="incrementerCompteurGame">+</button>
  <button @click="decrementerCompteurGame">-</button>
</template>

<script setup>

import {ref} from "vue";

const compteurGame = ref(0);

const incrementerCompteurGame = () => {
   this.compteurGame++
}

const decrementerCompteurGame = () => {
  this.compteurGame--
}


</script>

<style scoped>

</style>