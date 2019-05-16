<template>
  <section class="top-header">
    <div class="intro">
      <router-link to="/">
      <h1>Edward Williams</h1></router-link>
      <p>Hardware Tech + Web Developer</p>
    </div>
    <div class="profile">
      <a href="./eawilliams_resume.pdf" class="resume-btn">
        <span class="resume">
          <h2>RESUME</h2>
        </span>
      </a>
    </div>
  </section>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      msg: "Navigation Menu"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.top-header a:link,
.top-header h1 {
  color: var(--secondary);
}

.top-header p {
  font-size: 1.5rem;
  /* font-weight: 500; */
}

.top-header {
  padding: 30px;
  display: grid;
  height: auto;
  grid-auto-columns: 1fr;
  grid-template-areas: "intro profile";  
}

.intro {
  grid-area: intro;
  letter-spacing: 5px;
  font-size: 2rem;
  /* padding-top: 1.5rem; */
  text-align: center;
  align-items: center;
  /* background-color:rgba(0, 0, 0, 0.7);  */
}

.profile {
  display: flex;
  grid-area: profile;
  justify-items: center;
  align-items: center;
  padding: 0 auto;
  /* height: 100%; */
  font-size: 1.5rem;
  /* background-color:rgba(99, 0, 0, 0.7); */
  letter-spacing: 5px;
}

.resume-btn {
  color: var(--light);
  grid-area: name;
  font-size: 2rem;
  background: var(--secondary);
  margin: auto;
  padding: 1rem;
  /* height: 50px; */
  border-radius: var(--rounded);
  box-shadow: var(--shadow);
}

.profile .resume {
  color: var(--light);
}

.profile img {
  min-width: 150px;
  width: 50%;
  border-radius: 50%;
}
</style>
