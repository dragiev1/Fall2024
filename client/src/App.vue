<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue'
</script>

<template>
  <header>
    <NavBar />
  </header>

  <div class="container">
    <RouterView />
  </div>
</template>

<style scoped>
  .body { 
    background-color: gray;
  }
  .container {
    background-color: black;
    box-shadow: drop-shadow(0 0 10px rgb(255, 255, 255, 0.8));
    min-height: 100vh;
  }
</style>
