<script setup lang="ts">
const saludo: string = 'Hola a todos'
const botonHtml = "<button>Enviar</button>"
const color = "color: red"
const web = 'https://www.google.com'
const ahorro = 350
</script>

<template>
  <h1>Como están</h1>
  <h2>{{ saludo }}</h2>

  <span v-html="botonHtml"></span>

  <p :style="color">TEST</p>
  <a :href="web">Ir al sitio</a>

  <p :style="`color: ${ahorro > 100 ? 'green' : 'red'}`">{{ ahorro }}</p>
  <p :class="ahorro > 100 ? 'alto' : 'bajo'">{{ ahorro }}</p>
</template>

<style scoped>
h1 {
  font-size: 40px;
}

.bajo {
  color: red;
}

.alto {
  color: green;
}
</style>
