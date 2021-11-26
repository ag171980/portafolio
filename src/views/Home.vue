<template>
  <div class="home">
    <Background :content="myData"></Background>
    <About :content="myData"></About>
    <Skills :content="mySkills"></Skills>
    <Projects :content="myProjects"></Projects>
  </div>
</template>

<script>
import Background from "@/components/Background.vue";
import About from "@/components/About.vue";
import Skills from "@/components/Skills.vue";
import Projects from "@/components/Projects.vue";
export default {
  name: "Home",
  data() {
    return {
      myData: {
        name: "Alexis Gutierrez",
        img: "https://pbs.twimg.com/media/D4im7FnWkAEyPrz.jpg",
        puesto: "Frontend",
        edad: "22 años",
        carrera: "Ingeniería en Sistemas",
        developer: [{ nombre: "Frontend" }, { nombre: "Backend" }],
      },
      mySkills: [
        {
          img: "https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/1200px-HTML5_logo_and_wordmark.svg.png",
          filter: "Frontend",
          nombre: "Html 5",
        },
        {
          img: "https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/CSS3_logo_and_wordmark.svg/1452px-CSS3_logo_and_wordmark.svg.png",
          filter: "Frontend",
          nombre: "Css 3",
        },
        {
          img: "https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/1200px-Unofficial_JavaScript_logo_2.svg.png",
          filter: "Frontend",
          nombre: "Javascript",
        },
        {
          img: "https://cdn3.iconfinder.com/data/icons/logos-and-brands-adobe/512/288_Sass-512.png",
          filter: "Frontend",
          nombre: "Sass",
        },
        {
          img: "https://upload.wikimedia.org/wikipedia/commons/b/b2/Bootstrap_logo.svg",
          filter: "Frontend",
          nombre: "Bootstrap",
        },
        {
          img: "https://rmarketingdigital.com/wp-content/uploads/2020/12/nodejs-2451250.png",
          filter: "Backend",
          nombre: "Node JS",
        },
        {
          img: "https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/555px-Vue.js_Logo_2.svg.png",
          filter: "Frontend",
          nombre: "VueJS",
        },
        {
          img: "https://upload.wikimedia.org/wikipedia/commons/thumb/4/47/React.svg/1200px-React.svg.png",
          filter: "Frontend",
          nombre: "React",
        },
        {
          img: "https://www.joykal.com/wp-content/uploads/2019/09/jquery.png",
          filter: "Frontend",
          nombre: "Jquery",
        },
        {
          img: "https://images.tute.io/tute/topic/express-js.png",
          filter: "Backend",
          nombre: "Express",
        },
        {
          img: "https://www.onespan.com//sites/default/files/blog/images/logo-php-adbac78231.png",
          filter: "Backend",
          nombre: "PHP",
        },
        {
          img: "https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Laravel.svg/1200px-Laravel.svg.png",
          filter: "Backend",
          nombre: "Laravel",
        },
        {
          img: "https://d1.awsstatic.com/asset-repository/products/amazon-rds/1024px-MySQL.ff87215b43fd7292af172e2a5d9b844217262571.png",
          filter: "Backend",
          nombre: "MySQL",
        },
        {
          img: "https://cdn.worldvectorlogo.com/logos/figma-1.svg",
          filter: "Others",
          nombre: "Figma",
        },
        {
          img: "https://logodownload.org/wp-content/uploads/2019/10/adobe-photoshop-logo-1.png",
          filter: "Others",
          nombre: "Photoshop",
        },
        {
          img: "https://ivan6801.github.io/Portafolio-Ivan/sintaxis-img/postman.png",
          filter: "Others",
          nombre: "Postman",
        },
        {
          img: "https://cdn-icons-png.flaticon.com/512/25/25231.png",
          filter: "Others",
          nombre: "Github",
        },
        {
          img: "https://www.docker.com/sites/default/files/d8/2019-07/Moby-logo.png",
          filter: "Others",
          nombre: "Docker",
        },
      ],
      myProjects: {
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
            tecnologias: [
              "Html5",
              "Css3",
              "Sass",
              "Javascript",
              "MySQL",
              "php",
            ],
            nombre: "Amatista",
            repo: "",
            demo: "https://www.amatistamodayestilo.com.ar",
          },
          {
            img: require("../assets/imgProjects/amictus/amictus.png"),
            tecnologias: [
              "Html5",
              "Css3",
              "Sass",
              "Javascript",
              "MySQL",
              "php",
            ],
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
      },
    };
  },
  components: {
    Background,
    About,
    Skills,
    Projects,
  },
};
</script>
<style lang="scss">
@import "../scss/home.scss";
</style>
