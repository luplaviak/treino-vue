<template>
  <div class="componente">
    <h1>Componente Com Dados Não Reativos Primitivos</h1>
    <p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }}</p>
    <button v-on:click="fazerAniversario">Fazer Aniversário</button>
    <button @click="mudarNome()">Mudar Nome</button>
  </div>
</template>

<!-- <script setup>
import { reactive } from "vue";

const pessoa = reactive({
  nome: "Ana",
  idade: 27,
});

function fazerAniversario() {
  pessoa.idade += 1;
}
function mudarNome() {
  pessoa.nome = pessoa.nome === "Ana" ? "Ana Maria" : "Ana";
}
</script> -->

<script>
// options API
export default {
  data: function () {
    return { pessoa: { nome: "Ana", idade: 27 } };
  },
  methods: {
    fazerAniversario() {
      this.pessoa.idade += 1;
    },
    mudarNome() {
      this.pessoa.nome = this.pessoa.nome === "Ana" ? "Ana Maria" : "Ana";
    },
  },
};
</script>

<style scoped></style>
