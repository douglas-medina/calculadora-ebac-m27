<script setup>
import Calculadora from './components/Calculadora.vue';
</script>

<template>
  <header class="p-5 mb-4 mt-4 rounded-3">
    <h2>Calculadora Simples EBAC - VueJS</h2>
  </header>

  <br />
  <hr />

  <div class="p-2 mb-0 mt-1 rounded-3">
    <p>Para realizar uma operação simples, primeiro insira o primeiro número, após selecione a operação desejada, e, por último, insira o segundo número.</p>
  </div>

  <br />
  <hr />
  <Calculadora />
</template>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}
</style>