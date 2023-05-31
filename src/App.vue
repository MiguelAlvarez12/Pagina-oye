<template>
  <div id="app">
    <PaginaInicio />
    <CardContacto />
    <!-- Resto del contenido de tu aplicación -->
  </div>
</template>

<script>
import PaginaInicio from './components/PaginaInicio.vue';
import CardContacto from './components/CardContacto.vue'
export default {
  name: 'App',
  components: {
    PaginaInicio,
    CardContacto,
    
    
  },
};
</script>

<style>
/* Estilos de la aplicación */
</style>
