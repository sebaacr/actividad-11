# Actividad 11 - Feria Artesanal de Ñuble

## Descripción
Catálogo web interactivo, responsive y estructurado por componentes para la Feria Artesanal de Ñuble, desarrollado con Vue 3 y Vite.

## Conceptos de Vue aplicados
- **v-model**: Sincronización del buscador por texto y del selector de categorías.
- **v-if / v-else**: Alternancia entre la grilla de productos y el mensaje de "Sin resultados".
- **v-show**: Ocultar y mostrar el catálogo sin destruirlo del DOM.
- **v-for**: Renderizado dinámico de las tarjetas de productos y la lista de categorías.
- **computed**: Cálculo de la lista filtrada de productos y formateo del precio en CLP.
- **props y emits**: Paso de datos e interacción entre `App.vue`, `ProductoCard.vue` y `ProductoModal.vue`.

## Ejecución local
```bash
npm install
npm run dev