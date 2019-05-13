<template>
  <div class="footer">
    <!-- <div class="name">
                <a href="#">Edward Alexander Williams</a>
    </div>-->
    <div class="kiss-keep-it-simple-stupid">Simplicity & Functionality</div>
    <div class="email">
      <a href="mailto:edward.williams91@gmail.com">edward.williams91@gmail.com</a>
    </div>

    <div class="social">
      <img src="../assets/linkedin_logo.png" alt="Edward Williams' LinkedIn">
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      msg: "Navigation Menu"
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.footer {
  text-align: center;
  text-justify: auto;
  grid-gap: 20px;
  padding: 30px;
  display: grid;
  grid-auto-columns: 1fr;
  grid-template-areas:
    "name"
    "email"
    "social";
  margin-bottom: 40px;
}

.footer .name a {
  color: var(--light);
  grid-area: name;
  font-size: 2rem;
  background: var(--secondary);
  margin: auto;
  padding: 0.5rem;
  border-radius: var(--rounded);
  box-shadow: var(--shadow);
}

.footer .name a:hover,
a:visited,
a:link,
a:active {
  color: var(--light);
  text-decoration: none;
}

.footer .kiss-keep-it-simple-stupid {
  font-size: 1.5rem;
  text-decoration: underline;
}

.footer .email a {
  grid-area: email;
  font-size: 1.5rem;
}

.footer .email a,
a:hover,
a:visited,
a:link,
a:active {
  color: var(--alink);
  text-decoration: none;
}

.social img {
  height: 64px;
  box-shadow: var(--shadow);
  border-radius: var(--rounded);
}
</style>
