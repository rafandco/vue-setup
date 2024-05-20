<script setup>
const name = "Vue dinámico"
const stylecolor = "color: blue"
const arrayColores = ["blue", "red", "peru"]
const activo = true
</script>
<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <h2 :style="stylecolor">Soy azul</h2>
  <h2>{{ arrayColores }}</h2>
  <h2 :style="`color: ${arrayColores[2]}`">Soy Perú</h2>
  <h2>{{ activo ? "Estoy activo ternaria" : "Estoy inactivo ternaria" }}</h2>
  <h2 v-if="activo === true">Estoy activo v-if</h2>
  <p v-else-if="activo === false">Estoy inactivo v-else-if</p>
  <p v-else>Estoy indeciso v-else</p>
  <h2 v-show="activo">Estoy activo v-show</h2>
</template>
<style>
h1 {
  color: red;
}
</style>
