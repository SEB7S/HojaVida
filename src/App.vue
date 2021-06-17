<template>
  <div id="app" style="overflow-x: hidden">
    <div class="mb-2">
      <ul id="menu">
        <a href=""></a>
        <li><a href="#About" v-smooth-scroll>Acerca</a></li>
        <li><a href="#Experience" v-smooth-scroll>Experiencia</a></li>
        <li><a href="#Skills" v-smooth-scroll>Competencias</a></li>
        <li><a href="#Portafolio" v-smooth-scroll>Portafolio</a></li>
      </ul>
      <!--fim menu-->
    </div>
    <div v-scroll-reveal.reset="{ delay: 250 }" class="margin-about headline">
      <About id="About" />
    </div>
    <div>
      <Experience
        id="Experience"
        class="headline"
      />
    </div>
    <div class="margin-skills">
      <Skills id="Skills"  />
    </div>
    <div class="margin-portafolio">
      <Portafolio id="Portafolio" />
    </div>

    <!--     <Educacion id="Educacion" class="margin-educacion" /> -->

    <footer class="footer">© 2021 Copyright: sebastian Vera</footer>
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
  methods: {},
};
</script>

<style>
@import "./assets/styles/styles.scss";
.margin-about {
  margin-bottom: 500px !important;
}
.margin-skills {
  margin-bottom: 60%;
}
.margin-portafolio {
  margin-bottom: 10%;
}
.footer {
  background-color: #040c26;
  width: 100%;
  height: 100%;
  text-align: center !important;
  color: white;
}
</style>
