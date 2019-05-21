<template>
  <div class="project-details">
    <div class="project-left">
      <div class="project-header">
        <h1>Int to Roman</h1>
      </div>
      <div class="project-body">
        <p></p>
      </div>
    </div>

    <div class="project-right">
      <div class="project-header">
        <h1>{{msg}}</h1>
      </div>
      <div class="project-body">
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quo provident libero deserunt placeat iste quisquam. Rem a eum perspiciatis, natus sunt tempora facere laboriosam fugit porro quas deserunt maiores. Recusandae.</p>
      </div>
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
  </div>
</template>

<script>
export default {
  name: "About",
  data() {
    return {
      msg: "About Data"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.project-details {
  font-size: 1.5rem;
  color: var(--light);
  display: grid;

  grid-gap: 10px;
  grid-template-columns: 1fr 2fr;
  text-align: center;
  text-justify: auto;
}

.project-left {
  border-radius: var(--rounded);
  display: grid;
  grid-template-rows: 1fr 1fr 1fr;
  grid-template-areas:
    "project-header"
    "project-body";
  height: var(--card-height);
  box-shadow: var(--shadow);
  align-items: center;
  text-align: center;
  text-justify: auto;
  background-color: lightblue;
}

.project-right {
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
  background-color: orange;
}

.project-details img {
  height: 4rem;
  opacity: 1;
  margin: 0px;
  padding: 0px;
}
</style>
