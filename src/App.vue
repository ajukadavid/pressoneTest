<script setup lang="ts">
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue';
import Main from './components/Main.vue';
import Services from './components/Services.vue';
import Plans from './components/Plans.vue';

</script>

<template >
  <Navbar />
  <Hero />
  <Main />
  <Services />
  <Plans />
</template>

<style scoped>
.main {
  background: red;
  width: 100vw;
}
</style>
