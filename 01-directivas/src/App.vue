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
