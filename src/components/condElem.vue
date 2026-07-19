<script setup>
const isOnline = true;

const score = 80;
</script>

<template>
  <h2 v-if="isOnline">You are online</h2>
  <h2 v-else="isOnline">You are offline</h2>

  <h2 v-if="score >= 90">Excellent</h2>
  <h2 v-else-if="score >= 80 && score < 90">Good</h2>
  <h2 v-else>failed</h2>
</template>
