<script setup lang="ts">
import { onMounted } from 'vue';

onMounted(() => {
  if (localStorage.getItem('reloaded')) {

    localStorage.removeItem('reloaded');
  } else {
    localStorage.setItem('reloaded', '1');
    location.reload();
  }
})
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue';
import Main from './components/Main.vue';
import Services from './components/Services.vue';
import Plans from './components/Plans.vue';
import Footer from './components/Footer.vue';
</script>

<template >
  <Navbar />


  <Hero />
  <Main />
  <Services />
  <Plans />
  <Footer />
</template>

<style scoped></style>
