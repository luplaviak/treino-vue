<template>
  <div class="componente">
    <h1>Componente com Renderizacao Condicional</h1>
    <p>
      <strong>{{ nome }}</strong> {{ qtdGatos }}
    </p>
    <p v-if="qtdGatos === 0">Não tem gatos</p>
    <p v-else-if="qtdGatos === 1">Tem um gato</p>
    <p v-else="qtdGatos > 1">Tem muitos gatos</p>
  </div>
</template>

<script setup>
import { defineProps } from "vue";
defineProps({
  nome: String,
  qtdGatos: Number,
});
</script>

<style scoped></style>
