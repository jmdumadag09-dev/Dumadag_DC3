<template>
  <div class="card">
    <h2 :class="{ employee: employeeOfTheMonth }">
      {{ name }}
    </h2>
    <p>{{ department }}</p>
  </div>
</template>

<script setup>
defineProps({
  name: String,
  department: String,
  employeeOfTheMonth: Boolean,
});
</script>

<style>
.employee {
  color: purple;
  font-weight: bold;
}
</style>
