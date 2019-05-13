<template>
  <div class="projects">
    <ProjectCard v-for="project in projects" :key="projects"></ProjectCard>
  </div>
</template>

<script>
import ProjectCard from "./ProjectCard";

export default {
  name: "HelloWorld",
  components: {
    ProjectCard
  },
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      projects: {
        0: "Int to Roman",
        1: "Inventory",
        2: "Vue.js",
        3: "Insurance"
      }
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.projects {
  font-size: 1.5rem;
  color: var(--light);
  display: grid;
  grid-gap: 20px;
  grid-template-columns: repeat(4, 1fr);
  text-align: center;
  text-justify: auto;
}

.content p {
  font-size: 1.5rem;
  color: var(--light);
  display: grid;
  grid-gap: 20px;
  grid-template-columns: repeat(auto-fit, minmax(auto, 1fr));
  text-align: center;
  text-justify: auto;
  padding: 1rem;
}
</style>
