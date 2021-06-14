<template>
  <div>
    <div class="color-primary height"></div>
    <div class="w-50 d-flex flex-column align-items-center posicion-contenedor">
      <div class="text-white">
        <h3>Juan Sebastian Vera Betancur</h3>
        <p class="w-100 text-center">Desarrolador Web VUE / REACT / ANGULAR</p>
      </div>
      <div class="contenedor-img">
        <img src="../assets/img/profile.png" alt="..." class="rounded" />
      </div>

      <div
        class="
          cards
          text-center
          d-flex
          flex-column
          align-items-center
          justify-content-around
          pt-5
        "
      >
        <div class="texto mt-4">
          <a href="" class="mx-2"><i class="bi bi-whatsapp"></i></a>
          <a href="https://github.com/SEB7S" target="_blank" class="mx-2"
            ><i class="bi bi-github"></i
          ></a>
          <a
            href="https://www.linkedin.com/in/sebastian-vera-0130111b7/"
            target="_blank"
            class="mx-2"
            ><i class="bi bi-linkedin"></i
          ></a>
        </div>
        <div class="fuente">
          Ingeniero de Sistemas capacidades investigativas e informativas que
          permiten definir diseñar y construir, evaluar, auditar y mantener
          sistemas informativos. Habilidades en el desarrollo de aplicaciones
          web y móviles, corrección de fallas a nivel Hardware y Software en
          equipos de cómputo con planeación de estrategias para prevención de
          errores experiencia en la recuperación de sistemas afectados por
          software dañino y malintencionado. Conocimiento de: lenguajes de
          programación en JavaScript, Angular, Nodejs, Reactjs, aplicaciones
          web, bases de datos, lógica de programación, Blockchain y Contratos
          inteligentes.
        </div>
        <div class="d-flex justify-content-center w-100">
          <button type="button" class="btn btn-primary btn-sm w-25 mr-5">
            Descargar CV
          </button>
          <button type="button" class="btn btn-primary btn-sm w-25 mr-5">
            Contactar
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "About",
};
</script>
<style>
@import "../assets/styles/styles.scss";

.height {
  height: 200px;
  -webkit-box-shadow: 0px 7px 7px -4px rgba(0, 0, 0, 0.31);
  box-shadow: 0px 7px 7px -4px rgba(0, 0, 0, 0.31);
}

.posicion-contenedor {
  top: 10%;
  position: absolute;
  left: 0;
  right: 0;
  margin-left: auto;
  margin-right: auto;
}

.rounded {
  width: 145px;
  height: 150px;
  border: solid #6e6e6e;
  border-radius: 200px !important;
}

.texto a {
  font-size: 30px;
  color: black !important;
}

.fuente {
  font-family: "Courier New", Courier, monospace;
  text-align: justify !important;
  margin-bottom: 10px;
}

.cards {
  position: absolute;
  top: 80%;
  padding: 50px;
  height: 400px;
  -webkit-box-shadow: 0px 0px 25px -10px rgba(0, 0, 0, 0.81);
  box-shadow: 0px 0px 25px -10px rgba(0, 0, 0, 0.81);
}
.contenedor-img {
  z-index: 9999;
}
.btn-primary {
    color: #fff;
    background-color: #040c26 !important;
    border-color: #07174c !important;
}

.btn-primary:hover {
    color: #fff;
    background-color: #0c183d !important;
    border-color: #0c183d !important;
}
</style>