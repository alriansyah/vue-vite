<script setup>
import { ref } from "vue";
</script>

<template>
  <h1>
    --------------------------------Options API--------------------------------
  </h1>
  <div class="card">
    <div class="card-content">{{ count }}</div>
    <div class="card-actions">
      <!-- <button type="button" @click="count--">-</button>
      <button type="button" @click="count++">+</button> -->
      <button type="button" @click="decrement">-</button>
      <button type="button" @click="increment">+</button>
    </div>
  </div>
</template>

<style scoped>
.card {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  gap: 20px;
}

.card-content {
  font-size: 50px;
  font-weight: bold;
}

.card-actions {
  display: flex;
  gap: 20px;
}
</style>
