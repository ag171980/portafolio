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
  props:["content"],
  data() {
    return {
      nameFilters: ["All", "Frontend", "Backend", "Others"],
      filterActual: "All",
      idActual: 0,
      arrSkills: [],
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
        this.arrSkills = this.content;
      } else {
        var filterActual = this.filterActual;
        var arraySkills = this.arrSkills;
        this.content.forEach(function (valor) {
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