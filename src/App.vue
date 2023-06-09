<template>
  <div id="app">
    <PaginaInicio />
    <CardContacto />
    <PaginaCanciones />
    <!-- Resto del contenido de tu aplicación -->
  </div>
</template>

<script>
import PaginaInicio from './components/PaginaInicio.vue';
import CardContacto from './components/CardContacto.vue'
import PaginaCanciones from './components/PaginaCanciones.vue'
export default {
  name: 'App',
  components: {
    PaginaInicio,
    CardContacto,
    PaginaCanciones,
    
    
  },

};
</script>

<style>
/* Estilos de la aplicación */
</style>
