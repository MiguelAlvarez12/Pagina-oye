<template>
    <div class="navbar">
      <div class="navbar-left">
        <span class="Logo cursor-pointer">
        <img src="../assets/logo.png" alt="Logo" class="logo" />
      </span>
        <h1 class="title">OYE</h1>
      </div>
      <div class="navbar-center">
        <a class="linker" href="../components/PaginaInicio.vue">Inicio</a>
        <a class="linker linker-spaced" href="../components/PaginaCanciones.vue">Canciones</a>
        <PaginaCanciones/>
      </div>
       <div class="navbar-right">

        <div class="contacto">
      <span>
        <button class="button btn btn-primary" @click="mostrarModalContacto">Contacto</button>
        <CardContacto v-if="mostrarModal" @cerrarModal="ocultarModal" :estilos="modalEstilos"/>
      </span>

    </div>
        <button type="button" class="nav-btn btn btn-primary">Inicio de Sesión</button>
        <button type="button" class="nav-btn btn btn-primary">Registro</button>
      </div>
    </div>

    <div class="container d-flex align-items-center justify-content-center ">
    <div class="row">
      <div class="col-md-6">
        <h1 class="title2">Canciones gratis para la comunidad!</h1>
        <p class="text1">Con este sitio podras escuchar audios de manera libre...</p>
        <a class="a1 btn btn-primary" href="" role="button" >Ver Canciones</a>
      </div>
      <div class="col-md-6">
        <!-- <img src="../assets/portada.jpeg" alt="Imagen" class="img-fluid" /> -->
        <div id="carouselExampleSlidesOnly" class="carousel slide" data-bs-ride="carousel">
          <div class="carousel-inner">
            <div class="carousel-item active">
           <img src="../assets/portada.jpeg" class=" paso1 d-block img-fluid" alt="...">
          </div>
        <div class="carousel-item">
          <img src="../assets/portada.jpeg" class="paso2 d-block img-fluid" alt="...">
         </div>
    </div>
    </div>
      </div>
    </div>
  </div>

  <div class="container3 m-5">
    <div class="line"></div>
    <h1 class="title3">Top 3</h1>
    <div class="line"></div>
    <div class="row">
      <div class="col-5">
        <p class="text">Nombre</p>
      </div>
      <div class="col-7">
        <p class="text">Canción</p>
      </div>
      <div class="line"></div>
      <div class="row">
        <div class="col-5">
          <h3 class="subtitulo">Nuevamente</h3>
        </div>
        <div class="col-7">
          <audio controls class="audio">
            <source src="../canciones/uno.mp3" type="audio/mp3">
          </audio>
        </div>
      </div>
      <div class="line"></div>
      <div class="row">
        <div class="col-5">
          <h3 class="subtitulo">Suave</h3>
        </div>
        <div class="col-7">
          <audio controls class="audio">
            <source src="../canciones/dos.mp3" type="audio/mp3">
          </audio>
        </div>
      </div>
      <div class="line"></div>
      <div class="row">
        <div class="col-5">
          <h3 class="subtitulo">Alas</h3>
        </div>
        <div class="col-7">
          <audio controls class="audio">
            <source src="../canciones/tres.mp3" type="audio/mp3">
          </audio>
        </div>
        <div class="line"></div>
      </div>
    </div>

  </div>
  </template>
  
  <script>
  import '../styles/PaginaInicio.css'
  import CardContacto from './CardContacto.vue'
  import PaginaCanciones from './PaginaCanciones.vue'

export default {
  name:'PaginaInicio',
  components:{
    CardContacto,
    PaginaCanciones,
  },
  data(){
    return {
      mostrarModal: false,
      modalEstilos: {
        display:'none',
      },
    }
  },
  methods: {
    ocultarModal(){
      this.mostrarModal = false;
      this.modalEstilos = {
        display: 'none',
      }
    },
    mostrarModalContacto(){
      this.mostrarModal = true;
      this.modalEstilos = {
        display:'block',
      }
    },
  },
  mounted(){
    this.ocultarModal();
  },
}
  </script>

  <style></style>
