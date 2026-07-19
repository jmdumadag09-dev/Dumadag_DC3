<script setup>
const scores = [1, 2, 3, 4, 5, 6, 7, 8, 9];
</script>

<template>
  <h1>Scores</h1>
  <ul>
    <li v-for="score in scores" :key="score">
      {{ score }}
    </li>
  </ul>

  <p>Highest score:  }}</p>
</template>
