<template>
  <Navbar></Navbar>
  <div class="decoration">
    <div class="circulo cir"></div>
    <div class="circulo cir2"></div>
    <div class="circulo cir3"></div>
    <div class="circulo cir4"></div>
    <div class="cruz top"></div>
    <div class="cruz random"></div>
    <div class="cruz random1"></div>
    <div class="cruz middle"></div>
    <div class="cruz bottom"></div>
  </div>

  <router-view />
</template>
<script>
import Navbar from "@/components/Navbar.vue";

export default {
  name: "app",
  components: {
    Navbar,
  },
};
</script>
<style lang="scss">
@import "scss/partials/fonts";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background: #0f0f0f;
  height: 100vh;
}
.decoration {
  .circulo {
    height: 75px;
    width: 75px;
    background: none;
    position: fixed;
    border-radius: 40px;
    opacity: 0.6;
  }
  .cir,
  .cir4 {
    border: 10px solid #00ffff;
  }
  .cir2,
  .cir3 {
    border: 10px solid #c61ce4;
  }
  .cir {
    top: 15%;
    left: 25%;
  }
  .cir2 {
    top: 75%;
    left: 55%;
  }
  .cir3 {
    top: 55%;
    left: 5%;
  }
  .cir4 {
    top: 35%;
    left: 95%;
  }
  .cruz {
    position: fixed;
    height: 10px;
    width: 75px;
    border-radius: 10px;
    background-color: #c61ce4;
    transform: rotate(-45deg);
    opacity: 0.6;
    z-index: 1;
    &::before {
      content: "";
      position: fixed;
      top: 0;
      left: 0;
      transform: rotate(90deg);
      background-color: #c61ce4;
      height: 10px;
      width: 75px;
      border-radius: 10px;
    }
  }
  .top {
    top: 100px;
    left: 100px;
  }
  .middle {
    top: 50%;
    left: 45%;
    background-color: #00ffff;
    &::before {
      background-color: #00ffff;
    }
  }
  .random {
    top: 25%;
    left: 75%;
  }
  .random1 {
    top: 85%;
    left: 20%;
  }
  .bottom {
    bottom: 100px;
    right: 100px;
    background-color: #00ffff;
    &::before {
      background-color: #00ffff;
    }
  }
}
</style>
