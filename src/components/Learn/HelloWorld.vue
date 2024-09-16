<script setup>
import { ref } from "vue";

defineProps({
  msg: String,
});

const count = ref(0);

const decrement = () => {
  if (count.value > 0) {
    count.value--;
  }
};

const increment = () => {
  count.value++;
};
</script>

<template>
  <h1>{{ msg }}</h1>

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
