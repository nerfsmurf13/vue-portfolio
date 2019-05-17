<template>
  <div class="projects">
    <!-- <ProjectCard v-for="project in projects" :key="projects"></ProjectCard> -->

    <div
      class="project-card"
      v-for="project in projects"
      :key="project"
      style="background-image: url('../assets/projects_tech.jpg') center center no-repeat"
    >
      <router-link :to="project.route">
        <div class="project-header">
          <h1>{{project.name}}</h1>
        </div>
        <div class="project-body">{{project.img}}</div>
        <div class="project-footer">
          <img src="../assets/html_logo.png" alt="HTML Utilized">
          <img src="../assets/css_logo.png" alt="CSS Utilized">
          <img src="../assets/js_logo.png" alt="Javascript Utilized">
          <!--<img src="../images/nodejs_logo.png" alt="Node.js Utilized">
          <img src="../images/mongodb_logo.png" alt="MongoDB Utilized">-->
          <br>
          <img src="../assets/github_logo.png" alt="Github">
        </div>
      </router-link>
    </div>
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
      projects: [
        {
          name: "Int to Roman",
          route: "/about",
          img: "url('./assets/projects_tech.jpg') center center no-repeat;"
        },
        {
          name: "Inventory",
          route: "/",
          img: "../assets/projects_inventory.jpg"
        },
        {
          name: "Vue.js",
          route: "/",
          img: "../assets/projects_inventory.jpg"
        },
        {
          name: "Insurance",
          route: "/",
          img: "../assets/projects_inventory.jpg"
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
