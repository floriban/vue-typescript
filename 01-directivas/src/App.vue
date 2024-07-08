<script setup lang="ts">
const puntajeCrediticio = 800
const arrayEmoji = ['🍔', '🥞', '🍳', '🥐', '🥯', '🥖', '🍛', '🍲']
</script>

<template>
  <!-- V-IF -->
  <p v-if="puntajeCrediticio >= 900">Excelente cliente 😊</p>
  <p v-else-if="puntajeCrediticio < 900 && puntajeCrediticio >= 700">Cliente regular 😐</p>
  <p v-else>Pésimo cliente 😭</p>

  <!-- V-SHOW -->
  <p v-show="puntajeCrediticio >= 900">Excelente cliente 😊</p>
  <p v-show="puntajeCrediticio < 900 && puntajeCrediticio >= 700">Cliente regular 😐</p>
  <p v-show="puntajeCrediticio < 700">Pésimo cliente 😭</p>

  <!-- V-FOR -->
  <ul>
    <li v-for="(item, indice) in arrayEmoji" :key="indice">
      Emoji {{ item }}
    </li>
  </ul>

</template>

<style scoped></style>


const preguntasProgramacion = [
{
pregunta: "¿Cuál de los siguientes es un lenguaje de programación orientado a objetos?",
respuestas: [
"A) HTML",
"B) Java",
"C) CSS"
],
correcta: 1
},
{
pregunta: "¿Qué método se utiliza para unir dos arreglos en JavaScript?",
respuestas: [
"A) push()",
"B) concat()",
"C) join()"
],
correcta: 1
},
{
pregunta: "¿Cuál es el resultado de '2' + 2 en JavaScript?",
respuestas: [
"A) 22",
"B) 4",
"C) NaN"
],
correcta: 0
},
{
pregunta: "¿Qué significa SQL?",
respuestas: [
"A) Structured Query Language",
"B) Strong Question Language",
"C) Simple Query Language"
],
correcta: 0
},
{
pregunta: "¿Qué herramienta se utiliza para compilar programas escritos en C?",
respuestas: [
"A) Notepad",
"B) GCC",
"C) Photoshop"
],
correcta: 1
}
];
