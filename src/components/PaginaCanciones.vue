<template>
    <div>
      <!-- Navbar -->
      <div class="navbar">
        <div class="navbar-left">
          <img src="../assets/logo.png" alt="Logo" class="logo" />
          <h1 class="title">OYE</h1>
        </div>
        <div class="navbar-center">
          <router-link to="/pagina-inicio" class="nav-link">Inicio</router-link>
          <router-link to="/pagina-canciones" class="nav-link active">Canciones</router-link>
        </div>
        <div class="navbar-right">
          <div class="contacto">
            <button class="button btn btn-primary" @click="mostrarModalContacto">Contacto</button>
            <CardContacto v-if="mostrarModal" @cerrarModal="ocultarModal" :estilos="modalEstilos" />
          </div>
          <button type="button" class="nav-btn btn btn-primary">Inicio de Sesión</button>
          <button type="button" class="nav-btn btn btn-primary">Registro</button>
        </div>
      </div>
  
      <!-- Título y búsqueda -->
      <h2 class="titulo">Canciones</h2>
      <input type="text" class="input" placeholder="Buscar canciones" v-model="filtro" />
  
      <!-- Listado de canciones -->
      <div class="card-group">
        <div v-for="cancion in cancionesFiltradas" :key="cancion.nombre" class="card">
          <div class="card-body">
            <h5 class="card-title">{{ cancion.nombre }}</h5>
            <p class="card-text">Reproducciones: {{ cancion.reproducciones }}</p>
            <audio controls class="audio">
              <source :src="'../canciones/' + cancion.ruta" type="audio/mp3">
            </audio>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  import CardContacto from './CardContacto.vue';
  import cancionesData from '../data/datos.json';
  
  export default {
    name: 'PaginaCanciones',
    components: {
      CardContacto,
    },
    data() {
      return {
        mostrarModal: false,
        modalEstilos: {
          display: 'none',
        },
        filtro: '',
        canciones: [],
      };
    },
    methods: {
      ocultarModal() {
        this.mostrarModal = false;
        this.modalEstilos = {
          display: 'none',
        };
      },
      mostrarModalContacto() {
        this.mostrarModal = true;
        this.modalEstilos = {
          display: 'block',
        };
      },
    },
    computed: {
      cancionesFiltradas() {
        if (this.filtro === '') {
          return this.canciones;
        } else {
          const filtroLower = this.filtro.toLowerCase();
          return this.canciones.filter((cancion) =>
            cancion.nombre.toLowerCase().includes(filtroLower)
          );
        }
      },
    },
    mounted() {
      this.canciones = cancionesData.canciones;
    },
  };
  </script>
  
  <style>
  /* Estilos personalizados para la página de canciones */
  
  .titulo {
    font-size: 24px;
    margin-top: 20px;
  }
  
  .input {
    width: 80%;
    margin: 20px auto;
    padding: 10px;
    font-size: 16px;
  }
  
  .card-group {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
  }
  
  .card {
    width: 200px;
    text-align: center;
  }
  
  .audio {
    width: 100%;
  }
  
  /* Estilos para el navbar y otros componentes */
  
  /* ... (código CSS del navbar y otros componentes) ... */
  
  </style>
  