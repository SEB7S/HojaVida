<template>
  <div id="app">
    <div class="mb-2">
      <ul id="menu">
        <li><a href="#About">Acerca</a></li>
        <li><a href="#Experience">Experiencia</a></li>
        <li><a href="#Skills">Competencias</a></li>
        <li><a href="#Portafolio">Portafolio</a></li>
        <li><a href="#Educacion">Educación</a></li>
      </ul>
      <!--fim menu-->
    </div>

    <About id="About" class="margin-about" />
    <Experience id="Experience" />
    <Skills id="Skills" class="margin-skills"/>
    <Portafolio id="Portafolio" class="margin-portafolio" />
<!--     <Educacion id="Educacion" class="margin-educacion" /> -->

    

  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue' */

import About from "./components/About.vue";
import Experience from "./components/Experience.vue";
import Skills from "./components/Skills.vue";
/* import Educacion from "./components/Educacion.vue"; */
import Portafolio from "./components/Portafolio.vue";

export default {
  name: "App",
  components: {
    About,
    Experience,
    Skills,
    Portafolio,
/*     Educacion */
  },
};
</script>

<style>
@import "./assets/styles/styles.scss";
.margin-about{
  margin-bottom: 500px !important;
}
.margin-skills{
  margin-bottom: 60%;
}
</style>
