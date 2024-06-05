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
      <button type="button" @click="decrement">-</button>
      <button type="button" @click="increment">+</button>
    </div>
  </div>
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
