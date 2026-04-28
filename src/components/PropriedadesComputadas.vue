<template>
  <div class="componente">
    <h1>Componente com Propriedades Computadas</h1>
    <p>Idade: {{ idade }}</p>

    <label for="anonascimento">Ano Nascimento:</label>
    <input
      type="number"
      name="anonascimento"
      v-model="anoNascimento"
      min="1900"
    />
    <label for="anoatual">Ano Atual:</label>
    <input type="number" name="anoatual" v-model="anoAtual" min="2000" />
  </div>
</template>

<script setup>
import { ref, computed } from "vue";
const anoNascimento = ref(1900);
const anoAtual = ref(new Date().getFullYear());
const idade = computed(() => {
  return anoAtual.value - anoNascimento.value;
});
</script>

<style scoped>
label {
  margin: 10px;
}
</style>
