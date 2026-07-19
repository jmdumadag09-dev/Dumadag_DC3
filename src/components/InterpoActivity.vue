<script setup>
import { ref } from "vue";

const course = "Web Systems";
const instructor = "Mr. Reyes";
const room = "Lab 2";
const quizScore = 18;
const perfectScor = 20;
const score = ref(0);
const isOpen = ref(false);
const logo =
  "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTa2pv_KYLyBSvY4ytFS5yOSXACH41AK5nFO9L1rxsVXw&s=10";

const portal = "https://www.materdeicollege.com/";

const enrollDisabled = false;
</script>

<template>
  <div class="container">
    <h1>Vue.js Activity</h1>

    <h1>Task 1</h1>
    <h2>Course Information</h2>
    <p>Course:{{ course }}</p>
    <p>Instructor: {{ instructor }}</p>
    <p>Room: {{ room }}</p>

    <h1>Task 2</h1>
    <h2>Quiz Score</h2>
    <p>Quiz Score: {{ quizScore }}</p>
    <p>Perfect Score: {{ perfectScore }}</p>
    <p>Percentage: {{ (quizScore / perfectScore) * 100 }}%</p>

    <h1>Task 3</h1>
    <h2>Score</h2>
    <p>Score: {{ score }}</p>
    <button @click="score++">Add Point</button>

    <h1>Task 4</h1>
    <h2>Class Status</h2>
    <p>Class Status: {{ isOpen ? "Open" : "Closed" }}</p>
    <button @click="isOpen = !isOpen">Class Status</button>

    <h1>Task 5</h1>
    <h2>Task 5 - School Logo</h2>
    <img :src="logo" alt="School Logo" width="150" />

    <h1>Task 6</h1>
    <h2>School Portal</h2>
    <a :href="portal"> Visit School Portal </a>

    <h1>Task 7</h1>
    <h2>Enroll Button</h2>
    <button :disabled="enrollDisabled">Enroll</button>
  </div>
</template>
