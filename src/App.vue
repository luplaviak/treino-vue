<script setup>
import ComDados from "./components/ComDados.vue";
import ComDadosReativosNaoPrimitivos from "./components/ComDadosReativosNaoPrimitivos.vue";
import ComDadosReativosPrimitivos from "./components/ComDadosReativosPrimitivos.vue";
import ComProps from "./components/ComProps.vue";
import DataBinding from "./components/DataBinding.vue";
import EscutaEvento from "./components/EscutaEvento.vue";
import PrimeiroComponente from "./components/PrimeiroComponente.vue";
import PropriedadesAssistidas from "./components/PropriedadesAssistidas.vue";
import PropriedadesComputadas from "./components/PropriedadesComputadas.vue";
import RenderizacaoCondicional from "./components/RenderizacaoCondicional.vue";
import RenderizacaoListas from "./components/RenderizacaoListas.vue";
import Slots from "./components/Slots.vue";

const nomeItem = "Apontador";
const precoItem = 1.99;

const gatosDoJose = [
  { nome: "Bacana", idade: 3 },
  { nome: "Espeto", idade: 4 },
  { nome: "Xuxu", idade: 2 },
];
</script>

<template>
  <header>Treinamento Vue 3</header>
  <Slots>
    <!-- tabler icons -->
    <template v-slot:icone>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="currentColor"
        class="icon icon-tabler icons-tabler-filled icon-tabler-home"
      >
        <path stroke="none" d="M0 0h24v24H0z" fill="none" />
        <path
          d="M12.707 2.293l9 9c.63 .63 .184 1.707 -.707 1.707h-1v6a3 3 0 0 1 -3 3h-1v-7a3 3 0 0 0 -2.824 -2.995l-.176 -.005h-2a3 3 0 0 0 -3 3v7h-1a3 3 0 0 1 -3 -3v-6h-1c-.89 0 -1.337 -1.077 -.707 -1.707l9 -9a1 1 0 0 1 1.414 0m.293 11.707a1 1 0 0 1 1 1v7h-4v-7a1 1 0 0 1 .883 -.993l.117 -.007z"
        />
      </svg>
    </template>
    <template v-slot:texto> Home </template>
  </Slots>
  <Slots>
    <!-- tabler icons -->
    <template v-slot:icone>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="currentColor"
        class="icon icon-tabler icons-tabler-filled icon-tabler-home"
      >
        <path stroke="none" d="M0 0h24v24H0z" fill="none" />
        <path
          d="M12.707 2.293l9 9c.63 .63 .184 1.707 -.707 1.707h-1v6a3 3 0 0 1 -3 3h-1v-7a3 3 0 0 0 -2.824 -2.995l-.176 -.005h-2a3 3 0 0 0 -3 3v7h-1a3 3 0 0 1 -3 -3v-6h-1c-.89 0 -1.337 -1.077 -.707 -1.707l9 -9a1 1 0 0 1 1.414 0m.293 11.707a1 1 0 0 1 1 1v7h-4v-7a1 1 0 0 1 .883 -.993l.117 -.007z"
        />
      </svg>
    </template>
  </Slots>
  <RenderizacaoListas nome="Maria" :gatos="[]" />
  <RenderizacaoListas nome="Jose" :gatos="gatosDoJose" />
  <RenderizacaoCondicional nome="João" v-bind:qtdGatos="1" />
  <!-- <RenderizacaoCondicional nome="Maria" :qtdGatos="5" /> -->
  <PropriedadesAssistidas />
  <PropriedadesComputadas />
  <EscutaEvento />
  <!-- <ComProps item="Borracha" v-bind:preco="2.5" /> -->
  <ComProps item="Régua" :preco="9.0" />
  <ComProps :item="nomeItem" :preco="precoItem" />
  <DataBinding />
  <ComDadosReativosNaoPrimitivos />
  <ComDadosReativosPrimitivos />
  <ComDados />
  <PrimeiroComponente />
  <footer>
    <div style="margin: 30px">
      <a href="https://github.com/cod3rcursos/vuejs-masterclass" target="_blank"
        >Link do GitHub</a
      >
    </div>
  </footer>
</template>

<style scoped>
a {
  color: #007bff; /* Cor do link */
  text-decoration: none; /* Remove sublinhado */
  font-weight: bold; /* Negrito */
}
a:hover {
  color: #0056b3; /* Cor ao passar o mouse */
  text-decoration: underline; /* Sublinha ao passar o mouse */
}
a:visited {
  color: purple; /* Links já visitados */
}
</style>
