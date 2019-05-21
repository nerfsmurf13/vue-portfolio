<template>
  <div class="projects">
    <!-- <ProjectCard v-for="project in projects" :key="projects"></ProjectCard> -->

    <div v-for="project in projects" :key="project">
      <router-link :to="project.route">
        <div
          class="project-card"
          :style="{ background: 'url('+ project.img +') center center no-repeat', backgroundSize: 'cover'}"
        >
          <div class="project-header">
            <h1>{{project.name}}</h1>
          </div>
          <!-- <div class="project-body">{{project.tech}}</div> -->
          <div class="project-footer">
            <div>
              <img v-if="project.html" src="../assets/html_logo.png" alt="HTML Utilized">
              <img v-if="project.css" src="../assets/css_logo.png" alt="CSS Utilized">
              <img v-if="project.javascript" src="../assets/js_logo.png" alt="Javascript Utilized">
              <img v-if="project.vue" src="../assets/vue_logo.png" alt="Vue.js 2 Utilized">
              <img v-if="project.node" src="../assets/nodejs_logo.png" alt="Node.js Utilized">
              <img v-if="project.mongo" src="../assets/mongodb_logo.png" alt="MongoDB Utilized">
              <img v-if="project.mysql" src="../assets/mysql_logo.png" alt="MySQL Utilized">
              <img v-if="project.php" src="../assets/php_logo.png" alt="PHP Utilized">
            </div>
            <div>
              <img src="../assets/github_logo.png" alt="Github">
            </div>
          </div>
        </div>
      </router-link>
    </div>
  </div>
</template>

<script>
// import ProjectCard from "./ProjectCard";

export default {
  name: "HelloWorld",
  components: {},
  data() {
    return {
      projects: [
        {
          name: "Int to Roman",
          route: "/about",
          img: "http://edwardwilliams.me/images/projects_roman.jpg",
          git: "",
          html: true,
          css: true,
          javascript: true,
          mongo: false,
          mysql: false,
          node: false,
          php: false,
          vue: true
        },
        {
          name: "Inventory",
          route: "/",
          img: "http://edwardwilliams.me/images/projects_inventory.jpg",
          git: "",
          html: true,
          css: true,
          javascript: true,
          mongo: false,
          mysql: true,
          node: true,
          php: false,
          vue: false
        },
        {
          name: "Vue.js",
          route: "/",
          img: "http://edwardwilliams.me/images/projects_tech.jpg",
          git: "",
          html: true,
          css: true,
          javascript: true,
          mongo: false,
          mysql: false,
          node: false,
          php: false,
          vue: true
        },
        {
          name: "Insurance Form",
          route: "/",
          img: "http://edwardwilliams.me/images/projects_logs.jpg",
          git: "",
          html: true,
          css: true,
          javascript: true,
          mongo: false,
          mysql: false,
          node: false,
          php: false,
          vue: true
        }
      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
