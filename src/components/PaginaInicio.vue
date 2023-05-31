<template>
    <div class="navbar">
      <div class="navbar-left">
        <img src="../assets/logo.png" alt="Logo" class="logo" />
        <h1 class="title">OYE</h1>
      </div>
      <div class="navbar-center">
        <a to="../components/PaginaInicio.vue" class="nav-link" >Inicio</a>
        <!-- <router-link to="/canciones" class="nav-link" >Canciones</router-link> -->
      </div>
       <div class="navbar-right">
          
        <!-- <div class="contacto">
          <button type="button" class="nav-btn btn btn-primary" @click="showCardOnClick">Contacto</button>
           <CardContacto v-if="showCard" texto1="Texto 1 de la tarjeta"  texto2="Texto 2 de la tarjeta"/>
        </div> -->
        <div class="contacto">
      <span @click="showCardOnClick">
        <button class="button btn btn-primary">Contacto</button>
      </span>
      <CardContacto
        v-if="showCard"
        :texto1="hola"
        :texto2="texto "
      />
    </div>
        <button type="button" class="nav-btn btn btn-primary">Inicio de Sesión</button>
        <button type="button" class="nav-btn btn btn-primary">Registro</button>
      </div>
    </div>
    <!-- <div class="--bs-border-color">
      <div id="Carol">
        <figure>
  <blockquote class="blockquote">
    <h1>Canciones gratis para la <br>
    comunidad!</h1>
  </blockquote>
  <figcaption class="blockquote-footer">
    <cite title="Source Title">Con este sitio podras escuchar audios de manera libre...</cite>
  </figcaption>
</figure>
      </div>
    </div> -->
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
  <!-- <div class="container2 d-flex  justify-content-center flex-column">
    <div class="line"></div>
    <h1 class="title3">Título</h1>
    <div class="line"></div>
    <div class="row">
      <div class="col-md-6">
        <p class="text-left">Texto a la izquierda</p>
      </div>
      <div class="col-md-6 d-flex align-items-center justify-content-center">
        <p class="text-center">Texto al centro</p>
      </div>
    </div>
    <div class="line"></div>
    <div class="row">
      <div class="col-md-6">
        <h3 class="subtitle">Subtítulo a la izquierda</h3>
      </div>
      <div class="col-md-6 d-flex align-items-center justify-content-center">
        <audio controls class="audio">
          <source src="audio.mp3" type="audio/mpeg">
          Tu navegador no soporta el elemento de audio.
        </audio>
      </div>
    </div>
  </div> -->
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

  export default {
    name: 'PaginaInicio',

    components: {
      CardContacto,
    },
    data() {
    return {
      showCard: false,
    };
  },
  methods: {
    showCardOnClick() {
      this.showCard = true;
    },
  },
    
    // methods: {
    //   isRouteActive(route){
    //     return this.$route.path === route;
    //   }
    // }
  };
  </script>

  <style></style>
