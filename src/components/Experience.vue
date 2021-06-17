<template>
  <div>
    <div id="timeline">
      <h2 class="w-100 text-center">Experiencia</h2>
      <div class="demo-card-wrapper">
        <div class="demo-card demo-card--step1" v-scroll-reveal.reset="{ delay: 250 }">
          <div class="head">
            <div class="number-box">
              <span>01</span>
            </div>
            <h2><span class="small">Desarrollador</span> U. Manizales</h2>
          </div>
          <div class="body">
            <p><b>Universidad de Manizales</b></p>
            <p><b>01 de junio de 2019 - 31 de Diciembre 2020</b></p>

            <hr />
            <p><strong>Auxiliar de Desarrollo</strong></p>
            <ul>
              <li>Desarrollo de Plataformas web</li>
              <li>Soporte y Manetenimiento de Plataformas</li>
              <li>Desarrollo tecnología BlockChain</li>
            </ul>
            <hr />
            <ul>
              <li>CHEC EPM</li>
              <li>ElectroHuila</li>
              <li>Universidad de Manizales</li>
            </ul>
          </div>
        </div>

        <div class="demo-card demo-card--step2" v-scroll-reveal.reset="{ delay: 250 }">
          <div class="head">
            <div class="number-box">
              <span>02</span>
            </div>
            <h2><span class="small">Desarrollador</span>PROYECTIZA SAS</h2>
          </div>
          <div class="body">
            <p><b>Proyectiza SAS</b></p>
            <p><b>01 de julio de 2020- 31 de Octubre 2020</b></p>

            <hr />
            <p><strong>Desarrollador FrontEnd</strong></p>
            <ul>
              <li>Desarrollo de plataforma web <b>Dilisolver</b></li>
            </ul>
            <hr />
          </div>
        </div>

        <div class="demo-card demo-card--step3" v-scroll-reveal.reset="{ delay: 250 }"> 
          <div class="head">
            <div class="number-box">
              <span>03</span>
            </div>
            <h2><span class="small">Desarrollador</span> Price Shoes</h2>
          </div>
          <div class="body">
            <p><b>Price Shoes</b></p>
            <p><b>1 de enero de 2021- 31 de Junio 2021</b></p>

            <hr />
            <p><strong>Desarrollador FrontEnd</strong></p>
            <ul>
              <li>Desarrollo de plataforma web <b>PriceShoes</b></li>
            </ul>
            <hr />
          </div>
        </div>

        <div class="demo-card demo-card--step4" v-scroll-reveal.reset="{ delay: 250 }">
          <div class="head">
            <div class="number-box">
              <span>04</span>
            </div>
            <h2><span class="small">Desarrollador</span> Testiando</h2>
          </div>
          <div class="body">
            <p>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta
              reiciendis deserunt doloribus consequatur, laudantium odio dolorum
              laboriosam.
            </p>
          </div>
        </div>

        <div class="demo-card demo-card--step5" v-scroll-reveal.reset="{ delay: 250 }">
          <div class="head">
            <div class="number-box">
              <span>05</span>
            </div>
            <h2><span class="small">Subtitle</span> Conversion</h2>
          </div>
          <div class="body">
            <p>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta
              reiciendis deserunt doloribus consequatur, laudantium odio dolorum
              laboriosam.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Experience",
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
/* Media Queries */

@mixin mq-xs {
  @media (min-width: 320px) {
    @content;
  }
}

@mixin mq-sm {
  @media (min-width: 480px) {
    @content;
  }
}

@mixin mq-md {
  @media (min-width: 720px) {
    @content;
  }
}

@mixin mq-lg {
  @media (min-width: 1000px) {
    @content;
  }
}

$background: #ffffff;
$box-shadow: 0px 1px 22px 4px rgba(0, 0, 0, 0.07);
$border: 1px solid rgba(191, 191, 191, 0.4);
$items: 5;
$rows: ceil($items/2);

/* Card sizing */

$card-height: 400px;
$card-width: 450px;
$inner-margin: 15px;
$number-size: 35px;
$stagger: 180px;
$outer-margin: 90px;
$marker-size: 9px;

/* Colors */

$steps: #46b8e9;
$colors: #040c26, #040c26, #040c26, #040c26;
$timeline: #bdbdbd;

/* Calculations */

$container-height: $rows * ($card-height + $outer-margin) + $stagger;
$container-width: $card-width * 2 + $outer-margin * 3;
$head-height: $number-size + 50;
$body-height: $card-height - $head-height;
$marker-dist: $card-width + $outer-margin/2 - $marker-size/2;

/* Placeholders */

@include mq-lg {
  %arrow {
    position: absolute;
    content: "";
    width: 0;
    height: 0;
    border-top: 15px solid transparent;
    border-bottom: 15px solid transparent;
  }
  %marker {
    position: absolute;
    content: "";
    width: $marker-size;
    height: $marker-size;
    background-color: $timeline;
    border-radius: $marker-size;
    box-shadow: 0px 0px 2px 8px $background;
  }
}

/* Some Cool Stuff */

$counter: $items - $rows + 2;
@for $i from 1 through $rows {
  .demo-card:nth-child(#{$i*2-1}) {
    order: $i;
  }
  .demo-card:nth-child(#{$i*2}) {
    order: $counter;
  }
  $counter: $counter + 1;
}

/* Border Box */

* {
  box-sizing: border-box;
}

/* Fonts */

body {
  font-family: Roboto;
}

#timeline {
  background: $background;
  font-family: "Courier New", Courier, monospace !important;
  h1 {
    text-align: center;
    font-size: 3rem;
    font-weight: 200;
    margin-bottom: 20px;
  }
  p.leader {
    text-align: center;
    max-width: 90%;
    margin: auto;
    margin-bottom: 45px;
  }
  .demo-card-wrapper {
    position: relative;
    margin: auto;
    @include mq-lg {
      display: flex;
      flex-flow: column wrap;
      width: $container-width;
      height: $container-height;
      margin: 0 auto;
    }
    &::after {
      z-index: 1;
      content: "";
      position: absolute;
      top: 0;
      bottom: 0;
      left: 50%;
      border-left: $border;
      @include mq-lg {
        border-left: 1px solid $timeline;
      }
    }
  }
  .demo-card {
    position: relative;
    display: block;
    margin: 10px auto 80px;
    max-width: 94%;
    z-index: 2;
    @include mq-sm {
      max-width: 60%;
      box-shadow: $box-shadow;
    }
    @include mq-md {
      max-width: 40%;
    }
    @include mq-lg {
      max-width: $card-width;
      height: $card-height;
      margin: $outer-margin;
      margin-top: $outer-margin/2;
      margin-bottom: $outer-margin/2;
      &:nth-child(odd) {
        margin-right: $outer-margin/2;
        .head::after {
          @extend %arrow;
          border-left-width: 15px;
          border-left-style: solid;
          left: 100%;
        }
        .head::before {
          @extend %marker;
          left: $marker-dist + 1;
        }
      }
      &:nth-child(even) {
        margin-left: $outer-margin/2;
        .head::after {
          @extend %arrow;
          border-right-width: 15px;
          border-right-style: solid;
          right: 100%;
        }
        .head::before {
          @extend %marker;
          right: $marker-dist - 1;
        }
      }
      &:nth-child(2) {
        margin-top: $stagger;
      }
    }
    .head {
      position: relative;
      display: flex;
      align-items: center;
      color: #fff;
      font-weight: 400;
      .number-box {
        display: inline;
        float: left;
        margin: $inner-margin;
        padding: 10px;
        font-size: $number-size;
        line-height: $number-size;
        font-weight: 600;
        background: rgba(0, 0, 0, 0.17);
      }
      h2 {
        text-transform: uppercase;
        font-size: 1.3rem;
        font-weight: inherit;
        letter-spacing: 2px;
        margin: 0;
        padding-bottom: 6px;
        line-height: 1rem;
        @include mq-sm {
          font-size: 165%;
          line-height: 1.2rem;
        }
        span {
          display: block;
          font-size: 0.6rem;
          margin: 0;
          @include mq-sm {
            font-size: 0.8rem;
          }
        }
      }
    }
    .body {
      background: #fff;
      border: $border;
      border-top: 0;
      padding: $inner-margin;
      @include mq-lg {
        height: $body-height;
      }
      p {
        font-size: 14px;
        line-height: 18px;
        margin-bottom: $inner-margin;
      }
      img {
        display: block;
        width: 100%;
      }
    }
    @for $i from 1 through $items {
      &--step#{$i} {
        $color: nth($colors, ((($i - 1) % 4) + 1));
        background-color: $color;
        .head::after {
          border-color: $color;
        }
      }
    }
  }
}
</style>