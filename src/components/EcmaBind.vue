<script setup>

  defineProps({
    studentName: String,
    course: String,
    isEnrolled: Boolean
  });

</script>
<template>
   <h2>{{ studentName }}</h2>
    <p>Course: {{ course }}</p>
    
  <div :class="{ enrolled: isEnrolled }">
   <p>{{ isEnrolled ? "enrolled" : "Not Enrolled" }}</p>
  </div>
  
</template>

<style>
.enrolled {
  color: green;
  font-weight: bold;
}
</style>
