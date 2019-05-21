<template>
  <div id="app">
    <Header/>
    <!-- <router-link to="/about">About</router-link> -->
    <div class="content page">
      <transition
        name="router-anim"
        enter-active-class="animated slideInLeft"
        leave-active-class="animated slideOutRight"
        mode="out-in"
      >
        <router-view/>
      </transition>
    </div>
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/Header";
import Footer from "./components/Footer";

export default {
  name: "App",
  components: {
    Header,
    Footer
  }
};
</script>

<style>
/* @import "https://cdn.jsdelivr.net/npm/animate.css" */
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
:root {
  --primary: #ddd;
  --dark: #333;
  --light: #fff;
  --secondary: #0274b3;
  --shadow: 0 1px 5px rgba(104, 104, 104, 0.8);
  --card-height: 600px;
  --rounded: 5px;
}

html {
  font-family: "Anonymous Pro", monospace;
}

body {
  background: white;
  overflow-x: hidden;
}

body a {
  text-decoration: none;
}

body h1 {
  color: white;
  margin: 0;
  padding: 0;
}

body h2 {
  font-size: 2rem;
  margin: 0px;
  padding: 0px;
}

body p {
  margin: 0px;
  padding: 0px;
}
/* =====CONTENT===== */

.content {
  background: var(--primary);
  border-radius: var(--rounded);
  padding: 10px;
  max-height: inherit;
}

.page {
  /* position: fixed; */
  /* width: inherit; */
}

/* =====Content Contents===== */

.project-1 {
  grid-area: project-1;
  background: url("./assets/projects_roman.jpg") center center no-repeat;
  background-size: cover;
}

.project-1-img {
  background: url("./assets/projects_roman.jpg") center center no-repeat;
  background-size: cover;
}

.project-2 {
  grid-area: project-2;
  background: url("./assets/projects_inventory.jpg") center center no-repeat;
  background-size: cover;
}

.project-2-img {
  background: url("./assets/projects_inventory.jpg") center center no-repeat;
  background-size: cover;
}

.project-3 {
  grid-area: project-3;
  background: url("./assets/projects_tech.jpg") center center no-repeat;
  background-size: cover;
}

.project-4 {
  grid-area: project-4;
  background: url("./assets/projects_logs.jpg") center center no-repeat;
  background-size: cover;
}

.unfinished {
  background-color: rgba(255, 204, 0, 0.9);
  padding: 15px;
  /* margin: 0px;
  margin-bottom: px; */
}

.projects {
  font-size: 1.5rem;
  color: var(--light);
  display: grid;
  grid-gap: 10px;
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

.project-card:hover {
  transform: scale(1.01);
}

.project-card {
  border-radius: var(--rounded);
  display: grid;
  grid-template-rows: 1fr 1fr;
  grid-template-areas:
    "project-header"
    "project-footer";
  height: var(--card-height);
  box-shadow: var(--shadow);
  /* align-items: center;
  text-align: center;
  text-justify: auto; */
}

.project-header {
  grid-area: project-header;
  padding-top: 20px;
  padding-bottom: 20px;
  background-color: rgba(0, 0, 0, 0.7);
  align-self: center;
  /* width: 100%; */
}

.project-header h1 {
  text-decoration: none;
}

.project-body {
  /* margin: 20px; */
  /* background-color: yellow; */
  grid-area: project-body;
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
  grid-area: project-footer;
  padding-top: 20px;
  padding-bottom: 20px;
  background-color: rgba(255, 255, 255, 0.7);
  width: 100%;
  align-self: center;
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

@-webkit-keyframes slideInLeft {
  from {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    visibility: visible;
  }

  to {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }
}

@keyframes slideInLeft {
  from {
    -webkit-transform: translate3d(-100%, 0, 0);
    transform: translate3d(-100%, 0, 0);
    visibility: visible;
  }

  to {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }
}

.slideInLeft {
  -webkit-animation-name: slideInLeft;
  animation-name: slideInLeft;
  /* animation-duration: 25ms; */
}

@-webkit-keyframes slideOutRight {
  from {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }

  to {
    visibility: hidden;
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
  }
}

@keyframes slideOutRight {
  from {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }

  to {
    visibility: hidden;
    -webkit-transform: translate3d(100%, 0, 0);
    transform: translate3d(100%, 0, 0);
  }
}

.slideOutRight {
  -webkit-animation-name: slideOutRight;
  animation-name: slideOutRight;
}

.animated {
  -webkit-animation-duration: 1s;
  animation-duration: 1s;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
}
/* @media (print), (prefers-reduced-motion) {
  .animated {
    -webkit-animation: unset !important;
    animation: unset !important;
    -webkit-transition: none !important;
    transition: none !important;
  }
} */
@media (max-width: 1200px) {
  .projects {
    grid-template-columns: repeat(2, 1fr);
  }

  .top-header {
    grid-template-areas:
      "intro"
      "profile";
  }

  .intro p {
    margin-top: 15px;
  }

  .profile {
    margin-top: 20px;
    padding-top: 0;
  }
}

@media (max-width: 1000px) {
  /* ====Index==== */
  .projects {
    grid-template-columns: repeat(1, 1fr);
  }

  .top-header {
    grid-template-areas:
      "intro"
      "profile";
  }

  .profile {
    padding-top: 0;
  }

  /* ====Webapps Details==== */
  .project-details {
    grid-template-columns: 1fr;
    grid-template-areas:
      "details"
      "showcase";
  }
}
</style>
