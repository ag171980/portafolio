<template>
  <div class="projects" id="projects">
    <h2>Projects</h2>
    <div class="list-projects">
      <div class="project" v-for="(project, idp) in projects" :key="idp">
        <div
          class="img"
          :style="{
            background: 'url(' + project.img + ')',
            backgroundPosition: 'center',
            backgroundSize: 'cover',
          }"
        >
          <div class="description">
            <h3>{{ project.nombre }}</h3>
            <div class="tecnologias">
              <div
                class="tecnologia"
                v-for="(tecnologia, idt) in project.tecnologias"
                :key="idt"
              >
                <div class="color" v-for="(color, idc) in colors" :key="idc">
                  <p
                    v-if="color.nombre == tecnologia"
                    :style="{ background: color.color }"
                  >
                    {{ tecnologia }}
                  </p>
                </div>
              </div>
            </div>
            <div class="buttons">
              <a :href="project.repo" target="_blank">Repository</a>
              <a :href="project.demo" target="_blank">Demo</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Projects",
  data() {
    return {
      colors: [
        {
          nombre: "Html5",
          color: "#FF9E00",
        },
        {
          nombre: "Css3",
          color: "#187DFF",
        },
        {
          nombre: "Sass",
          color: "#F974FF",
        },
        {
          nombre: "Javascript",
          color: "#FFFF00",
        },
        {
          nombre: "MySQL",
          color: "#FFB15D",
        },
        {
          nombre: "php",
          color: "#5D9BFF",
        },
        {
          nombre: "Jquery",
          color: "#89B4F0",
        },
        {
          nombre: "Vue",
          color: "#03B800",
        },
        {
          nombre: "MongoDB",
          color: "#8CFF8A",
        },
        {
          nombre: "Laravel",
          color: "#FF3E27",
        },
      ],
      projects: [
        {
          img: require("../assets/imgProjects/portfolio/portfolio.png"),
          tecnologias: ["Vue", "Sass"],
          nombre: "Portfolio",
          repo: "https://github.com/ag171980/portafolio",
          demo: "https://portfolionicolas.netlify.app",
        },
        {
          img: "https://capacitacion.neuquen.gov.ar/wp-content/uploads/2020/01/225-2256239_web-en-construccion-png-sitio-en-construccion.jpg",
          tecnologias: ["Vue", "MongoDB", "Laravel"],
          nombre: "Spotifake",
          repo: "",
          demo: "",
        },
        {
          img: require("../assets/imgProjects/weatherapp/weather.png"),
          tecnologias: ["Html5", "Css3", "Javascript"],
          nombre: "Weather App",
          repo: "https://github.com/ag171980/weather-app",
          demo: "https://ag171980.github.io/weather-app/",
        },
        {
          img: require("../assets/imgProjects/amatista/amatista.png"),
          tecnologias: ["Html5", "Css3", "Sass", "Javascript", "MySQL", "php"],
          nombre: "Amatista",
          repo: "",
          demo: "https://www.amatistamodayestilo.com.ar",
        },
        {
          img: require("../assets/imgProjects/amictus/amictus.png"),
          tecnologias: ["Html5", "Css3", "Sass", "Javascript", "MySQL", "php"],
          nombre: "Amictus",
          repo: "https://github.com/Gol-inc/amictus",
          demo: "",
        },
        {
          img: require("../assets/imgProjects/brugge/brugge.png"),
          tecnologias: ["Html5", "Css3", "Sass", "Javascript", "Jquery"],
          nombre: "Brugge",
          repo: "https://github.com/ag171980/brugge",
          demo: "https://ag171980.github.io/brugge/",
        },
        {
          img: require("../assets/imgProjects/hotel/hotelpanoramas.png"),
          tecnologias: ["Html5", "Css3", "Javascript"],
          nombre: "Hotel Panorama's",
          repo: "https://github.com/ag171980/pagina-hoteleria",
          demo: "https://ag171980.github.io/pagina-hoteleria/index.html",
        },
        {
          img: require("../assets/imgProjects/cddelc/cddelc.png"),
          tecnologias: ["Vue", "Sass"],
          nombre: "Casa de Dios en Las Calles",
          repo: "https://github.com/ag171980/cddelc",
          demo: "https://casa-de-dios-4f04d.firebaseapp.com",
        },
        {
          img: require("../assets/imgProjects/tgif/tgif.png"),
          tecnologias: ["Html5", "Css3", "Javascript"],
          nombre: "TGIF",
          repo: "https://github.com/ag171980/TGIF-Alexis-",
          demo: "https://ag171980.github.io/TGIF-Alexis-/",
        },
      ],
    };
  },
};
</script>