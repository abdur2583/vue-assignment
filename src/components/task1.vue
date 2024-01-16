<script setup>
import { ref, reactive } from 'vue'
 const data = reactive([{ name: 'Task 1', time: 60}, { name: 'Task 2', time: 75},{ name: 'Task 3', time: 95}]);
</script>

<template>
  <div class="container">
    <h2>from task 1</h2>
  </div>
</template>

<style scoped>

</style>
