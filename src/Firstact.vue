<script setup>
import { computed } from "vue";

const fruit = ["apple", "banana", "orange", "mango"];
const isOnline = true;
const hasAccount = true;
const students = ["jian", "bro", "jed", "alaniel", "harvey"];
const totalStudents = computed(() => students.length);
</script>

<template>
  <h1>Fruitas</h1>
  <ul>
    <li v-for="fruit in fruit" :key="fruit">{{ fruit }}</li>
  </ul>

  <h2 v-if="isOnline">Your are Online</h2>
  <h2 v-if="hasAccount">Welcome User</h2>
  <h2 v-else>Please Register</h2>
  <h2>Total Students: {{ totalStudents }}</h2>
</template>
