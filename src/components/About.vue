<template>
  <div class="project-card project-1">
                    <div class="project-header">
                        <h1>{{msg}}</h1>
                    </div>
                    <div class="project-body">
                            
                    </div>
                    <div class="project-footer">
                        <img src="../assets/html_logo.png" alt="HTML Utilized">
                        <img src="../assets/css_logo.png" alt="CSS Utilized">
                        <img src="../assets/js_logo.png" alt="Javascript Utilized">
                        <!--<img src="../images/nodejs_logo.png" alt="Node.js Utilized">
                        <img src="../images/mongodb_logo.png" alt="MongoDB Utilized">-->
                        </br>
                        <img src="../assets/github_logo.png" alt="Github">
                    </div>
                </div>
</template>

<script>
export default {
  name: 'About',
  data () {
    return {
      msg: 'About Data'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
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
</style>
