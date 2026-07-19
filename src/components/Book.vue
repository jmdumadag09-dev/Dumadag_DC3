<template>
  <div :class="{sold: isSold}">
    <h2>{{ bookName }}</h2>
    <p>Author: {{ author }}</p>
    <p>{{ isSold ? "Sold" : "Available" }}</p>
  </div>
</template>

<script>
export default {
  props: {
    bookName: String,
    author: String,
    isSold: Boolean
  }
};
</script>

<style>
.sold {
  color: red;
  font-weight: bold;
}
</style>
