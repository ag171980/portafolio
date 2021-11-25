<template>
  <div class="background" id="home">
    <div class="img">
      <Foto></Foto>
      <div class="circle"></div>
    </div>
    <div class="descripcion">
      <h1>{{ nombre }}</h1>
      <p>{{ puesto }} Developer</p>
      <div class="buttons">
        <div class="button" v-for="(dev, idx) in developer" :key="idx">
          <p @mouseover="showDev(dev.nombre)">{{ dev.nombre }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Foto from "@/components/Foto.vue";
export default {
  name: "Background",
  components: {
    Foto,
  },
  data() {
    return {
      nombre: "Alexis Gutierrez",
      puesto: "Frontend",
      developer: [{ nombre: "Frontend" }, { nombre: "Backend" }],
    };
  },
  methods: {
    showDev(puesto) {
      this.puesto = puesto;
    },
  },
};
</script>