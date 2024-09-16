<script setup></script>

<template>
  <div class="container">
    <header>
      <h1 class="header-title">Memo</h1>
      <button class="header-button" type="button">+</button>
    </header>
    <main>
        <div>[card]</div>
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
</style>
