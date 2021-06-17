<template>
  <div class="texto row d-flex justify-content-center">
    <h2 class="w-100 text-center">Portafolio</h2>
    <div
      class="card text-white bg-primary mb-3 mx-3 col-lg-4"
      style="max-width: 18rem"
      v-scroll-reveal.reset="{ delay: 250 }"
    >
      <div class="card-header">Cultura y Servicio</div>
      <div class="card-body">
        <h5 class="card-title">Universidad de Manizales</h5>
        <p class="card-text">
          Plataforma dedicada a la gestion de información necesaria para la
          suministración de inforación relacionada con la Universidad de
          Manizales.
        </p>
        <a href=""></a>
      </div>
    </div>
    <div
      class="card text-white bg-primary mb-3 mx-3 col-lg-4"
      style="max-width: 18rem"
      v-scroll-reveal.reset="{ delay: 350 }"
    >
      <div class="card-header">Dilisolver</div>
      <div class="card-body">
        <h5 class="card-title">Proyectiza SAS</h5>
        <p class="card-text">
          Plataforma dedicada a la gestion de diligencias a nivel empresarial.
        </p>
        <a href="https://www.dilisolver.com/" target="balnked"
          >Dilisolver.com</a
        >
      </div>
    </div>
    <div
      class="card text-white bg-primary mb-3 mx-3 col-lg-4"
      style="max-width: 18rem"
      v-scroll-reveal.reset="{ delay: 450 }"
    >
      <div class="card-header">Control y Gestion de la Informacion</div>
      <div class="card-body">
        <h5 class="card-title">PriceShoes</h5>
        <p class="card-text">Plataforma orientada a la gestión empresarial</p>
        <a href="https://priceshoes.vercel.app/" target="balnked"
          >priceshoes.com</a
        >
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Portafolio",
  module: {
    rules: [
      // ... other rules omitted

      // this will apply to both plain `.scss` files
      // AND `<style lang="scss">` blocks in `.vue` files
      {
        test: /\.scss$/,
        use: ["vue-style-loader", "css-loader", "sass-loader"],
      },
    ],
  },
};
</script>
<style lang="scss">
.texto {
  font-family: "Courier New", Courier, monospace !important;
}
.card-header {
  padding: 0.75rem 1.25rem;
  margin-bottom: 0;
  background-color: rgba(0, 0, 0, 0.03) !important;
  border-bottom: 1px solid rgb(255 255 255);
}
.bg-primary {
  background-color: #040c26 !important;
}

.texto a {
  font-size: 15px !important;
  color: white !important;
}
</style>