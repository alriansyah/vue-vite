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
      <div class="form-overlay">
        <div class="form-modal">
          <button class="form-close-button">&times;</button>
          <textarea name="memo" id="memo" cols="30" rows="10"></textarea>
          <button class="form-save-button">Save</button>
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
