<template>
  <div class="texto">
    <h2 class="w-100 text-center">Portafolio</h2>
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
</style>