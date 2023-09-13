<script setup lang="ts">
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue';
import Main from './components/Main.vue';
</script>

<template >
  <Navbar />
  <Hero />
  <Main />
</template>

<style scoped>
.main {
  background: red;
  width: 100vw;
}
</style>
