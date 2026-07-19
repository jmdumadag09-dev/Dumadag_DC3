<script setup>
import { ref } from "vue";

const score = ref(85);
</script>
<template>
  <div>
    <p v-if="score >= 90">Grade: A</p>
    <p v-else-if="score >= 80">Grade: B</p>
    <p v-else-if="score >= 75">Grade: C</p>
    <p v-else>Failed</p>
  </div>
</template>
