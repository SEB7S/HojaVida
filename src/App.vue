<template>
  <div id="app">
    <div class="mb-2">
      <ul id="menu">
        <li><a href="#">Acerca</a></li>
        <li><a href="#">Experiencia</a></li>
        <li><a href="#">Habilidades</a></li>
        <li><a href="#">Portafolio</a></li>
        <li><a href="#">Educación</a></li>
      </ul>
      <!--fim menu-->
    </div>

    <About class="margin-about" />
    <Experience />

  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue' */

import About from "./components/About.vue";
import Experience from "./components/Experience.vue";

export default {
  name: "App",
  components: {
    About,
    Experience,
  },
};
</script>

<style>
@import "./assets/styles/styles.scss";
.margin-about{
  margin-bottom: 500px !important;
}
</style>
