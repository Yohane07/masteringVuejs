<script setup lang="ts">
import Person from './components/Person.vue';
import Modifiers from "./components/Modifiers.vue";
import FormVmodelRef from "./components/FormVmodelRef.vue";
import ComputedOption from "./components/ComputedOption.vue";
import TailWindTest from "./components/TailWindTest.vue";
import {ref} from "vue";

const impressionEnDirect = ref("");

</script>

<template>
  <header>
    <TailWindTest/>
    <input type="text" v-model="impressionEnDirect">
    <p>{{impressionEnDirect}}</p>
    <Modifiers/>
    <div>
      <p>Let's go testeer avec</p>
      <Person/>
      <FormVmodelRef/>
      <hr>
    </div>
    <hr>
    <div>
      <ComputedOption/>
    </div>
  </header>
</template>

<style>

</style>
