<template>
  <div class="background" id="home">
    <div class="img">
      <Foto :img="content.img"></Foto>
      <div class="circle"></div>
    </div>
    <div class="descripcion">
      <h1>{{ content.name }}</h1>
      <p>{{ puesto }} Developer</p>
      <div class="buttons">
        <div class="button" v-for="(dev, idx) in content.developer" :key="idx">
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
  props: ["content"],
  components: {
    Foto,
  },
  data() {
    return {
      name: "Alexis Gutierrez",
      puesto: "Frontend",
    };
  },
  methods: {
    showDev(puesto) {
      // this.$emit('puesto',puesto);
      this.puesto = puesto;
    },
  },
};
</script>