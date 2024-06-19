<script setup >
import { reactive, ref } from "vue";

const count = ref(0);
const listData = reactive([]);

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
  <h1>
    --------------------------------Composition
    API--------------------------------
  </h1>
  <div class="card">
    <div class="card-content">{{ count }}</div>
    <div class="card-actions">
      <button type="button" @click="decrement">-</button>
      <button type="button" @click="increment">+</button>
    </div>
  </div>
</template>

<style scoped>
h1 {
  font-size: 20px;
}
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
