<template>
  <div class="skills" id="skills">
    <h2>Skills</h2>
    <div class="filters">
      <p
        @click="filter(nameFilter, idf)"
        class="filter"
        v-for="(nameFilter, idf) in nameFilters"
        :key="idf"
      >
        {{ nameFilter }}
      </p>
    </div>
    <div class="list-skills">
      <div class="skill" v-for="(skill, idx) in arrSkills" :key="idx">
        <img :src="skill.img" alt="" />
        <div class="skill-description">
          <p>{{ skill.nombre }}</p>
          <p></p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Skills",
  data() {
    return {
      nameFilters: ["All", "Frontend", "Backend", "Others"],
      filterActual: "All",
      idActual: 0,
      arrSkills: [],
      skills: [
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
    };
  },
  methods: {
    filter(name, id) {
      this.arrSkills = [];
      this.filterActual = name;
      document.getElementsByClassName("filter")[this.idActual].classList.remove("active");
      this.idActual = id;
      document.getElementsByClassName("filter")[id].classList.add("active");
      if (this.filterActual == "All") {
        this.arrSkills = this.skills;
      } else {
        var filterActual = this.filterActual;
        var arraySkills = this.arrSkills;
        this.skills.forEach(function (valor) {
          if (valor.filter == filterActual) {
            arraySkills.push({
              img: valor.img,
              filter: valor.filter,
              nombre: valor.nombre,
            });
          }
        });
        this.arrSkills = arraySkills;
      }
    },
  },
  mounted() {
    this.filter(this.filterActual, this.idActual);
  },
};
</script>