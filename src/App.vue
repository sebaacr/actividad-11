<script setup>
import { RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
</script>

<template>
  <Navbar />
  <main>
    <RouterView />
  </main>
  <footer class="footer-app">
    <p>Feria Artesanal de Ñuble · Actividad 12</p>
  </footer>
</template>