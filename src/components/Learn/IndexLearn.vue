<script setup>
import HelloWorld from "./HelloWorld.vue";
import OptionsApi from "./OptionsApi.vue";
import CompositionApi from "./CompositionApi.vue";
</script>

<template>
  <HelloWorld msg="Vite + Vue" />
  <OptionsApi />
  <CompositionApi />
</template>

<style scoped>
:root {
  font-family: Inter, system-ui, Avenir, Helvetica, Arial, sans-serif;
  line-height: 1.5;
  font-weight: 400;

  color-scheme: light dark;
  color: rgba(255, 255, 255, 0.87);
  background-color: #242424;

  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

body {
  margin: 0;
  display: flex;
  place-items: center;
  min-width: 320px;
  min-height: 100vh;
}

h1 {
  font-size: 3.2em;
  line-height: 1.1;
}

button {
  width: 100px;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 8px;
  font-size: 30px;
  font-weight: bold;
  font-family: inherit;
  background-color: #1a1a1a;
  cursor: pointer;
  border: 1px solid #ffffff;
  transition: border-color 0.25s;
}
button:hover {
  border-color: #646cff;
}

#app {
  max-width: 1280px;
  margin: 0 auto;
  text-align: center;
}
</style>
