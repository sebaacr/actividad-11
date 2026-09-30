<script setup>
import { computed } from 'vue'
import { useRoute, RouterLink } from 'vue-router'
import { productos } from '../data/productos'

const route = useRoute()
const producto = computed(() => {
  return productos.find(p => p.id === Number(route.params.id))
})
</script>

<template>
  <section class="pagina">
    <div v-if="producto" class="detalle-producto">
      <img :src="producto.imagen" :alt="producto.nombre" />
      <div>
        <span class="categoria">{{ producto.categoria }}</span>
        <h1>{{ producto.nombre }}</h1>
        <p><strong>Comuna:</strong> {{ producto.comuna }}</p>
        <p>{{ producto.descripcion }}</p>
        <h2>${{ producto.precio.toLocaleString('es-CL') }}</h2>
        <RouterLink to="/productos" class="btn-volver">← Volver al catálogo</RouterLink>
      </div>
    </div>
    <div v-else>
      <h2>Producto no encontrado</h2>
      <RouterLink to="/productos">Volver al catálogo</RouterLink>
    </div>
  </section>
</template>