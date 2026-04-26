<template>
  <div class="componente">
    <h1>Componente com Data Binding</h1>
    <p>{{ valor }}</p>
    <!-- one way data binding -->
    <!-- <input type="text" v-bind:value="valor" /> -->

    <!-- two way data binding -->
    <!-- com diretiva v-bind : e v-on @ -->
    <!-- <input
      type="text"
      v-bind:value="valor"
      v-on:input="(e) => (valor = e.target.value)"
    /> -->
    <!-- <input
      type="text"
      :value="valor"
      @input="(e) => (valor = e.target.value)"
    /> -->
    <!-- com diretiva v-model -->
    <input type="text" v-model="valor" />
  </div>
</template>

<script setup>
import { ref } from "vue";
const valor = ref("Vue é muito legal");
console.log(valor.value);
</script>

<style scoped></style>
