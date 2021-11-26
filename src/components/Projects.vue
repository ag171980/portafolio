<template>
  <div class="projects" id="projects">
    <h2>Projects</h2>
    <div class="list-projects">
      <div
        class="project"
        v-for="(project, idp) in content.projects"
        :key="idp"
      >
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
                <div
                  class="color"
                  v-for="(color, idc) in content.colors"
                  :key="idc"
                >
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
  props: ["content"],
};
</script>