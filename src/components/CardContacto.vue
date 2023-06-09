<template>
  <div class="modal" :style="estilos" v-show="mostrarModal">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Contacto</h5>
          <button type="button" class="btn-close" @click="cerrarModal" aria-label="Close"></button>
        </div>
        <div class="modal-body">
          <p>info@oye.com</p>
          <p>+57 301 692 9337</p>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-primary" @click="cerrarModal" data-bs-dismiss="modal">Close</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import '../styles/CardContacto.css'
export default {
  name: 'CardContacto',
  props: {
    estilos: {
      type: Object,
      default: () => ({}),
    },
  },
  data() {
    return {
      mostrarModal: false,
    };
  },
  methods: {
    cerrarModal() {
      this.mostrarModal = false;
      this.$emit('cerrarModal');
    },
  },
};
</script>

<style>

</style>

