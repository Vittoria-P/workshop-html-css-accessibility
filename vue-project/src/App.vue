<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Hero from './components/Hero.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <Hero />
  <main>
    <RouterView />
  </main>
  <Footer />
</template>