<script setup>
import { ref } from "vue";

const showForm = ref(false);
const newMemo = ref("");
const memos = ref([]);

const handleShowForm = () => {
  showForm.value = true;
}

const getRandomColor = () => {
  return `#${Math.floor(Math.random() * 16777215).toString(16)}`
}

const addMemo = () => {
  memos.value.push({
    id: Date.now(),
    memo: newMemo.value,
    date: new Date().toLocaleDateString("en-GB"),
    backgroundColor: getRandomColor(),
  });

  newMemo.value = "";
  showForm.value = false;
}
</script>

<template>
  <div class="container">
    <header>
      <h1 class="header-title">Memo</h1>
      <button @click="handleShowForm" class="header-button" type="button">+</button>
    </header>
    <main>
      <div class="card-container">
        <div v-for="memo in memos" class="card" :key="memo.id" :style="{ backgroundColor: memo.backgroundColor }">
          <p class="card-content">{{ memo.memo }}
          </p>
          <p>{{ memo.date }}</p>
        </div>
      </div>
      <div v-if="showForm" class="form-overlay">
        <div class="form-modal">
          <button @click="showForm = false" class="form-close-button">&times;</button>
          <textarea v-model="newMemo" name="memo" id="memo" cols="30" rows="10"></textarea>
          <button @click="addMemo" class="form-save-button">Save</button>
        </div>
      </div>
    </main>
  </div>
</template>

<style scoped>
#app {
  width: 100vw;
  height: 100vh;
}

.container {
  max-width: 80%;
  padding: 10px;
  margin: 0 auto;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header-title {
  font-size: 48px;
  font-weight: bold;
  margin-bottom: 25px;
  color: #495a7d;
}

.header-button {
  border: none;
  padding: 10px;
  width: 50px;
  height: 50px;
  cursor: pointer;
  border-radius: 100%;
  background-color: #495a7d;
  color: #fff;
}

.card-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}

.card {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 225px;
  height: 225px;
  padding: 10px;
  background-color: #ffa6c1;
  /* border-radius: ; */
  margin-bottom: 20px;
}

.form-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.77);
  z-index: 10;
  display: flex;
  justify-content: center;
  align-items: center;
}

.form-modal {
  position: relative;
  width: 500px;
  background-color: #fff;
  border-radius: 10px;
  padding: 30px;
  display: flex;
  flex-direction: column;
}

.form-save-button {
  padding: 10px 20px;
  font-size: 20px;
  width: 100%;
  background-color: #495a7d;
  color: #fff;
  border: none;
  cursor: pointer;
  border-radius: 5px;
  margin-top: 15px;
}

.form-close-button {
  position: absolute;
  top: 3px;
  right: 10px;
  width: 30px;
  height: 30px;
  background-color: transparent;
  font-size: 30px;
  cursor: pointer;
  border: none;
}
</style>
