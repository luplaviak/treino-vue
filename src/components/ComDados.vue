<template>
  <div class="componente">
    <h2>Componente com dados</h2>
    <p>Nome: Caneta - #123</p>
    <p>Nome: {{ nomeProduto }} - {{ codigoProduto }}</p>
  </div>
</template>

<script setup>
const nomeProduto = "Apontador";
const codigoProduto = "#987";
</script>

<!-- <script>
//options API   forma mais antiga vue 2
// export default {
//   data: function () {
//     return {
//       nomeProduto: "Caderno",
//       codigoProduto: "#321",
//     };
//   },
// };

//composition API
// export default {
//   setup: function () {
//     const nomeProduto = "Lápis";
//     const codigoProduto = "#789";
//     return {
//       codigoProduto,
//       nomeProduto,
//     };
//   },
// };
</script> -->

<style scoped></style>
