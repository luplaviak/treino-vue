<script setup>
import ComDados from "./components/ComDados.vue";
import ComDadosReativosNaoPrimitivos from "./components/ComDadosReativosNaoPrimitivos.vue";
import ComDadosReativosPrimitivos from "./components/ComDadosReativosPrimitivos.vue";
import ComProps from "./components/ComProps.vue";
import DataBinding from "./components/DataBinding.vue";
import PrimeiroComponente from "./components/PrimeiroComponente.vue";
</script>

<template>
  <header>Vue</header>
  <!-- <ComProps item="Borracha" v-bind:preco="2.5" /> -->
  <ComProps item="Régua" :preco="9.0" />
  <DataBinding />
  <ComDadosReativosNaoPrimitivos />
  <ComDadosReativosPrimitivos />
  <ComDados />
  <PrimeiroComponente />
</template>

<style scoped></style>
