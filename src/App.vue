<script setup lang="ts">
import Home from './views/Home.vue';
</script>

<template>
  <div class="wrapper">
    <Home />
  </div>
</template>

<style>

body {
  background: #000;
  margin: 0;
  padding: 0;
}

#app {
  margin: 0;
  padding: 0;
}

.wrapper {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
