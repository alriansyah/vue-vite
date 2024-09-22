<script setup></script>

<template>
  <div class="container">
    <header>
      <h1 class="header-title">Memo</h1>
      <button class="header-button" type="button">+</button>
    </header>
    <main>
      <div class="card-container">
        <div class="card">
          <p class="card-content">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatum eius iste corporis, fugiat deleniti
            maxime. Repudiandae, ipsa. Sunt, itaque illum?
          </p>
          <p>22/09/2024</p>
        </div>
        <div class="card">
          <p class="card-content">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatum eius iste corporis, fugiat deleniti
            maxime. Repudiandae, ipsa. Sunt, itaque illum?
          </p>
          <p>22/09/2024</p>
        </div>
        <div class="card">
          <p class="card-content">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptatum eius iste corporis, fugiat deleniti
            maxime. Repudiandae, ipsa. Sunt, itaque illum?
          </p>
          <p>22/09/2024</p>
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
</style>
