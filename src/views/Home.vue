<template>
  <div class="home">
    <Background></Background>
    <About></About>
    <Skills></Skills>
    <Projects></Projects>
  </div>
</template>

<script>
import Background from "@/components/Background.vue";
import About from "@/components/About.vue";
import Skills from "@/components/Skills.vue";
import Projects from "@/components/Projects.vue";
export default {
  name: "Home",
  components: {
    Background,
    About,
    Skills,
    Projects
  },
};
</script>
<style lang="scss">
@import "../scss/home.scss";
</style>
