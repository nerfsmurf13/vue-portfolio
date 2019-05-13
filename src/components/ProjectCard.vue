<template>
  <div class="project-card">
    <div class="project-header">
      <h1>{{projects[projects]}}</h1>
    </div>
    <div class="project-body"></div>
    <div class="project-footer">
      <img src="../assets/html_logo.png" alt="HTML Utilized">
      <img src="../assets/css_logo.png" alt="CSS Utilized">
      <img src="../assets/js_logo.png" alt="Javascript Utilized">
      <!--<img src="../images/nodejs_logo.png" alt="Node.js Utilized">
      <img src="../images/mongodb_logo.png" alt="MongoDB Utilized">-->
      <br>
      <img src="../assets/github_logo.png" alt="Github">
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectCard",
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
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.project-card:hover {
  transform: scale(1.01);
}

.project-card {
  border-radius: var(--rounded);
  display: grid;
  grid-template-rows: 1fr 1fr 1fr;
  grid-template-areas:
    "project-header"
    "project-body"
    "project-footer";
  height: var(--card-height);
  box-shadow: var(--shadow);
  align-items: center;
  text-align: center;
  text-justify: auto;
}

.project-header {
  padding-top: 20px;
  padding-bottom: 20px;
  background-color: rgba(0, 0, 0, 0.7);
  width: 100%;
}

.project-body {
  /* margin: 20px; */
  /* background-color: yellow; */
  margin: 0 20px 40px 20px;
  color: black;
  font-size: 1.5rem;
  /* background-color: rgba(0, 0, 0, 0.7);
  width: 100%; */
}

.project-body p {
  padding: 1rem 0;
  color: white;
}

.project-body p a {
  background-color: #32b259;
  color: white;
  padding: 1rem;
  border-radius: var(--rounded);
  box-shadow: var(--shadow);
}

.project-footer {
  padding-top: 20px;
  padding-bottom: 20px;
  background-color: rgba(255, 255, 255, 0.7);
  width: 100%;
}

.project-card img {
  height: 4rem;
  opacity: 1;
  margin: 0px;
  padding: 0px;
}

.project-card-details img {
  height: 4rem;
  opacity: 1;
  margin: 0px;
  padding: 0px;
}
</style>
