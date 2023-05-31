<template>
  <div class="card-container" v-if="showCard">
    <div class="card">
      <div class="card-header">
        <h4 class="card-title">Contacto</h4>
        <button class="close" @click="closeCard">&times;</button>
      </div>
      <div class="card-body">
        <p>{{ texto1 }}</p>
        <p>{{ texto2 }}</p>
      </div>
      <div class="card-footer">
        <button class="btn btn-secondary" @click="closeCard">Cerrar</button>
      </div>
    </div>
  </div>
</template>
  
  <script>
  export default {
    name:'CardContacto',

    data() {
      return {
        showCard: false,
      };
    },
    props: {
      texto1: {
        type: String,
        required: true,
      },
      texto2: {
        type: String,
        required: true,
      },
    },
    methods: {
      closeCard() {
        this.showCard = false;
      },
      showCardOnClick() {
      this.showCard = true;
    },
    },
  };
  </script>
  
  <style>
  .card-container {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 9999;
  }
  
  .card {
    width: 300px;
    background-color: #fff;
    border-radius: 4px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .card-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px;
    background-color: #f2f2f2;
    border-bottom: 1px solid #ccc;
  }
  
  .card-title {
    margin: 0;
  }
  
  .close {
    cursor: pointer;
    border: none;
    background: none;
    font-size: 20px;
    color: #333;
  }
  
  .card-body {
    padding: 10px;
  }
  
  .card-footer {
    display: flex;
    justify-content: flex-end;
    padding: 10px;
    background-color: #f2f2f2;
    border-top: 1px solid #ccc;
  }
  </style>
  