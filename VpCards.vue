<template>
  <div class="vue-projects-cards">
    <a
      v-for="project in projects"
      class="vue-projects-card"
      :href="project.href"
      target="_blank"
    >
      <img
        :alt="project.title + ' logo'"
        class="vue-projects-image"
        :src="'https://TheJaredWilcurt.com/vue-projects/images/' + project.src"
      />
      <span
        v-html="project.title"
        class="vue-projects-title"
      ></span>
      <span
        v-html="project.description"
        class="vue-projects-description"
      ></span>
    </a>
  </div>
</template>

<script>
export default {
  name: 'VueProjectsCards',
  data: function () {
    return {
      projects: [
        {
          description: 'Vue Component Documentation',
          href: 'https://TheJaredWilcurt.com/vue-doxen',
          src: 'doxen.png',
          title: 'Vue-Doxen'
        },
        {
          description: 'Accessibility plugin for<br/>Vite-Vue-DevTools',
          href: 'https://vue-dev-tools-accessibility.github.io',
          src: 'vdta.svg',
          title: 'Vue-Dev-Tools-Accessibility'
        },
        {
          description: 'Vue unit testing tool',
          href: 'https://TheJaredWilcurt.com/vue-snapshot-serializer',
          src: 'vss.png',
          title: 'Vue-Snapshot-Serializer'
        },
        {
          description: 'Vue Desktop App Boilerplate',
          href: 'https://github.com/nwutils/nw-vue3-boilerplate',
          src: 'nw-vue.png',
          title: 'NW.js + Vue 3'
        }
        // Constants plugin
        // Options API Boilerplate
      ]
    };
  }
};
</script>

<style>
.vue-projects-cards {
  display: flex;
  flex-direction: row;
  align-items: start;
  justify-content: center;
  gap: 1rem;
}
.vue-projects-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  max-width: 200px;
  color: currentColor;
  text-decoration: none;
}
.vue-projects-image {
  max-width: 100px;
  max-height: 100px;
  background-color: #FFFFFF05;
  border-radius: 8px;
  box-shadow: 2px 2px 5px #0006;
  transition: 0.5s ease transform;
}
.vue-projects-card:hover .vue-projects-image {
  transform: scale(1.05);
}
.vue-projects-title {
  margin: 0.5rem 0rem;
  font-size: 1.1rem;
  text-align: center;
}
.vue-projects-description {
  font-size: 0.8rem;
  text-align: center;
  opacity: 0.65;
}
</style>
