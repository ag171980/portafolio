<template>
  <div class="about" id="aboutme">
    <h2>About Me</h2>
    <div class="card">
      <Foto :img="content.img"></Foto>
      <div class="description">
        <h3>{{content.name}}</h3>
        <p>
          Tengo 21 años y actualmente estoy estudiando
          <span>Ingeniería en Sistemas</span>. A la vez, de forma autodidacta
          estudio para ser un <span>Desarrollador Frontend</span>, capacitándome
          en las últimas tecnologías.<br />
          Me encuentro en la búsqueda de un trabajo que me permita <span>crecer tanto
          profesionalmente como personalmente</span>, uno donde pueda <span>aportar mis
          conocimientos y aprender del equipo</span>.<br />
          En mis tiempos libres me gusta seguir aprendiendo haciendo cursos,
          salir con mi perro, ver series y fútbol.
        </p>
      </div>
    </div>
  </div>
</template>
<script>
import Foto from "@/components/Foto.vue";
export default {
  name: "About",
  props:["content"],
  components: {
    Foto,
  },
};
</script>
<style lang="scss">
</style>