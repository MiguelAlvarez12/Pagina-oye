<template>
    <div class="navbar">
      <div class="navbar-left">
        <img src="../assets/logo.png" alt="Logo" class="logo" />
        <h1 class="title">OYE</h1>
      </div>
      <div class="navbar-center">
        <router-link to="../components/PaginaInicio.vue" class="nav-link" >Inicio</router-link>
        <router-link to="/canciones" class="nav-link" >Canciones</router-link>
      </div>
      <div class="navbar-right">
        <button type="button" class="nav-btn btn btn-primary">Contacto</button>
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
  <div class="container2 d-flex align-items-center justify-content-center flex-column">
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
  </div>
  </template>
  
  <script>
  export default {
    name: 'PaginaInicio',
    // methods: {
    //   isRouteActive(route){
    //     return this.$route.path === route;
    //   }
    // }
  };
  </script>

  <style>

    /* Estilos para la barra de navegacion */

  .navbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    background-color: #f2f2f2;
    padding: 10px;
  }
  
  .navbar-left {
    display: flex;
    align-items: center;
  }
  
  .logo {
    width: 40px;
    height: 40px;
    margin-right: 10px;
  }
  
  .title {
    font-size: 3em;
    font-weight: bold;
    padding: 0;
    margin: 0;
    color:rgb(0, 110, 255);
  }
  
  .navbar-center {
    display: flex;
  }
  
  .nav-link {
    margin-right: 10px;
    text-decoration: none;
    color: #333;
  }

  .nav-link.active {
  font-weight: bold;
  }
  
  .navbar-right {
    display: flex;
  }
  
  .nav-btn {
    margin-right: 10px;
    padding: 5px 10px;
    cursor: pointer;
  }

    /* Estilos para contenedor de informacion */

  .container {
  background-color: #c2bdbdb6;
  padding: 20px;
  margin-top: 20px;
  height: 40vh; /* Ajusta el contenedor al 100% del alto de la ventana */
  padding: 0.5em;
}

.row {
  margin: 0 auto; /* Centra el contenido horizontalmente */
}

.title2 {
  margin-top: 5%;
  font-weight: bold;
}

.img-fluid {
  max-width: 70%;
  height: auto;
  margin: 1em;
}

.text1 {
  margin-top: 3%;
}

.a1 {
  margin-top: 4%;
}

.paso2 {
  -webkit-filter: invert(100%);
  filter: invert(100%);
}

    /* Estilos para top 3 canciones */

.line {
  width: 68.8%;
  height: 1px;
  background-color: #ccc;
  margin-bottom: 10px;
  margin-top: 5%;
}

.title3 {
  font-size: 2em;
    font-weight: bold;
    padding: 0;
    margin: 0;
    color:rgb(0, 110, 255);
}

.text-left {
  text-align: left;
}



</style>