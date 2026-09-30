<script setup>
import { RouterLink } from 'vue-router'

defineProps({
  producto: {
    type: Object,
    required: true
  },
  favorito: {
    type: Boolean,
    default: false
  }
})

const emit = defineEmits(['cambiar-favorito'])
</script>

<template>
  <article class="producto-card">
    <img :src="producto.imagen" :alt="producto.nombre" />
    <div class="contenido-producto">
      <span class="categoria">{{ producto.categoria }}</span>
      <h3>{{ producto.nombre }}</h3>
      <p class="comuna">{{ producto.comuna }}</p>
      <strong>${{ producto.precio.toLocaleString('es-CL') }}</strong>
      <div class="acciones">
        <RouterLink :to="`/productos/${producto.id}`" class="btn-detalle">
          Ver detalle
        </RouterLink>
        <button class="btn-fav" @click="emit('cambiar-favorito', producto.id)">
          {{ favorito ? '★ Favorito' : '☆ Agregar' }}
        </button>
      </div>
    </div>
  </article>
</template>