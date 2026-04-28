<template>
  <div class="componente">
    <h1>Componente com Slots</h1>
    <div class="box">
      <!-- <button><slot></slot></button> -->
      <button>
        <slot name="icone" /> <slot name="texto">Texto Padrão</slot>
      </button>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.box {
  display: flex;
  justify-content: center;
}
button {
  display: flex;
  align-items: center;
  gap: 10px;
  cursor: pointer;
  border-radius: 50px;
}
</style>
