<template>
  <nav class="navbar">
    <a href="#home">Home</a>
    <a href="#aboutme">About Me</a>
    <a href="#skills">Skills</a>
    <a href="#projects">Projects</a>
    <div class="contacts">
      <i class="fab fa-github"></i>
      <i class="far fa-envelope"></i>
      <i class="fab fa-linkedin-in"></i>
    </div>
  </nav>
</template>
<style lang="scss">
</style>
<script>
export default {
  name: "Navbar",
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