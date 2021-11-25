<template>
  <nav class="navbar">
    <a href="#home">Home</a>
    <a href="#aboutme">About Me</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>

    <div class="btn-menu" @click="modalMenu()">
      <div class="bar"></div>
    </div>
    <div class="menu-dropdown" :class="{ show: stateModal }">
      <a href="#home" @click="modalMenu()">Home</a>
      <a href="#aboutme" @click="modalMenu()">About Me</a>
      <a href="#skills" @click="modalMenu()">Skills</a>
      <a href="#projects" @click="modalMenu()">Projects</a>
    </div>

    <div class="contacts">
      <a href="https://github.com/ag171980" target="_blank"><i class="fab fa-github"></i></a>
      <a href="mailto:gutierrezalexisnicolas@gmail.com" target="_blank"><i class="far fa-envelope"></i></a>
      <a href="https://www.linkedin.com/in/alexis-nicolas-gutierrez/" target="_blank"><i class="fab fa-linkedin-in"></i></a>
    </div>
  </nav>
</template>
<style lang="scss">
</style>
<script>
export default {
  name: "Navbar",
  data() {
    return {
      stateModal: false,
    };
  },
  methods: {
    modalMenu() {
      if (this.stateModal) {
        this.stateModal = false;
      } else {
        this.stateModal = true;
      }
    },
  },
  mounted() {
    let recaptchaScript = document.createElement("script");
    recaptchaScript.setAttribute(
      "src",
      "https://kit.fontawesome.com/5b23b3e9e6.js"
    );
    document.head.appendChild(recaptchaScript);
  },
};
</script>