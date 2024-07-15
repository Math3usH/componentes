<script setup>
import ExpandBox from './components/ExpandBox.vue';
const caixas = [
  {id: 1, title: "caixa 1", content: "conteudo 1", quantity: 100},
  {id: 2, title: "caixa 2"},
  {id: 3, title: "caixa 3", quantity: 100},
  {id: 4, title: "caixa 4", content: "conteudo 4"}
]
</script>

<template>
  <h1>componentes</h1>
  <expand-box v-for="caixa in caixas" :key="caixas.id" v-bind="caixa" />
  <!-- <ExpandBox title="Caixa 1" content="conteudo 1" />
  <ExpandBox title="Caixa 2" content="conteudo 2" />
  <ExpandBox title="Caixa 3" /> -->
</template>

<style scoped></style>