<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <section class="pagina pagina-404">
    <h1>404</h1>
    <h2>Página no encontrada</h2>
    <p>La dirección solicitada no existe.</p>
    <RouterLink to="/">Regresar al inicio</RouterLink>
  </section>
</template>