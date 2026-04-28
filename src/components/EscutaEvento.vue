<template>
  <div class="componente">
    <h1>Componente que Escuta Evento</h1>
    <p>Qtde Itens: {{ qtde }}</p>
    <p>Valor Total: R$ {{ total.toFixed(2) }}</p>
    <button @click="esvaziarCarrinho">Esvaziar o Carrinho</button>
    <div class="lista">
      <EmiteEvento
        item="Item 1"
        :preco="1.99"
        @foiAdicionado="atualizarTotal"
      />
      <EmiteEvento item="Item 2" :preco="5.0" @foiAdicionado="atualizarTotal" />
      <EmiteEvento
        item="Item 3"
        :preco="10.99"
        @foiAdicionado="atualizarTotal"
      />
    </div>
  </div>
</template>

<script setup>
import EmiteEvento from "./EmiteEvento.vue";
import { ref } from "vue";
const qtde = ref(0);
const total = ref(0);
function atualizarTotal(p) {
  total.value = +(total.value + p).toFixed(2);
  // const valor = total.value + p;
  // total.value = +valor.toFixed(2);
  qtde.value += 1;
  console.log("atualizarTotal");
}

function esvaziarCarrinho() {
  qtde.value = 0;
  total.value = 0;
}
</script>

<style scoped>
.lista {
  display: flex;
  justify-content: space-between;
}
</style>
