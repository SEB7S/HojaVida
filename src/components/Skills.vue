<template>
  <div class="skills">
    <div class="charts">
      <h2 class="w-100 m-5 text-center">Competencias</h2>
      <div class="chart chart--dev">
        <div class="card p-5 my-3" v-scroll-reveal.reset="{ delay: 250 }">
          <h5 class="m-3">Profesionales:</h5>
          <ul class="chart--horiz">
            <li class="chart__bar" style="width: 90%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> HTML5 </span>
                <span class="chart__label w-100 mr-2 texto-end"> 90% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 85%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> CSS & SCSS & CSS3</span>
                <span class="chart__label w-100 mr-2 texto-end"> 85% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 70%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> JavaScript </span>
                <span class="chart__label w-100 mr-2 texto-end"> 70% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 60%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> ReactJS </span>
                <span class="chart__label w-100 mr-2 texto-end"> 60% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 90%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> Angular </span>
                <span class="chart__label w-100 mr-2 texto-end"> 90% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 70%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> VueJS </span>
                <span class="chart__label w-100 mr-2 texto-end"> 70% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 70%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> NodeJS </span>
                <span class="chart__label w-100 mr-2 texto-end"> 70% </span>
              </div>
            </li>
          </ul>
        </div>
        <div class="card p-5 my-3" v-scroll-reveal.reset="{ delay: 250 }">
          <h5 class="m-3">Personales:</h5>
          <ul class="chart--horiz">
            <li class="chart__bar" style="width: 90%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> Compromiso </span>
                <span class="chart__label w-100 mr-2 texto-end"> 90% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 95%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100">Puntualidad</span>
                <span class="chart__label w-100 mr-2 texto-end"> 95% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 80%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> Liderazgo </span>
                <span class="chart__label w-100 mr-2 texto-end"> 80% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 85%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> Comunicación </span>
                <span class="chart__label w-100 mr-2 texto-end"> 85% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 95%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> Capaciad Analítica </span>
                <span class="chart__label w-100 mr-2 texto-end"> 95% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 90%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> Trabajo en Equipo </span>
                <span class="chart__label w-100 mr-2 texto-end"> 90% </span>
              </div>
            </li>
            <li class="chart__bar" style="width: 97%">
              <div class="w-100 d-flex">
                <span class="chart__label w-100"> Actitud </span>
                <span class="chart__label w-100 mr-2 texto-end"> 97% </span>
              </div>
            </li>
          </ul>
        </div>
        
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Skills",
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
@import url(https://fonts.googleapis.com/css?family=Open+Sans);

@mixin stagger-anim-delay($i, $initial-delay, $stagger-delay) {
  @while $i > 0 {
    &:nth-of-type(#{$i}) {
      animation-delay: $initial-delay + $stagger-delay * $i;
    }
    $i: $i - 1;
  }
}

$baseFontSize: 16px;
$baseLineHeight: 1;

$chartGap: 10px;
$chartCount: 3;
$chartOneCount: 11;
$chartTwoCount: 2;
$chartThreeCount: 4;
$totalChartCount: $chartOneCount + $chartTwoCount + $chartThreeCount;

$titleGap: 10px;
$titleHeight: $baseFontSize * $baseLineHeight + $titleGap;

$chartBarHeight: 30px;
$chartBarGap: 10px;

.texto-end {
  text-align: end !important;
}
.skills {
  width: 80%;
  max-width: 960px;
  height: 780px;
  height: 100%;
  margin: auto;
  font-family: "Courier New", Courier, monospace !important;
  position: relative;
}

.lines {
  height: 100%;
  position: relative;
}
.line {
  height: inherit;
  width: 2px;

  position: absolute;

  background: rgba(#eee, 0.6);

  &.l--0 {
    left: 0;
  }
  &.l--25 {
    left: 25%;
  }
  &.l--50 {
    left: 50%;
  }
  &.l--75 {
    left: 75%;
  }
  &.l--100 {
    left: calc(100% - 1px);
  }
}
.line__label {
  display: block;
  width: 100px;
  text-align: center;

  position: absolute;
  bottom: -20px;
  right: -50px;

  &.title {
    text-transform: uppercase;
    font-weight: bold;
  }
}

.charts {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 10;
}

.chart {
  &:not(:first-child) {
    margin-top: $chartGap;
  }
}

.chart__title {
  display: block;
  margin: 0 0 10px;

  font-weight: bold;

  opacity: 0;

  animation: 1s anim-lightspeed-in ease forwards;

  .chart--dev & {
  }
  .chart--prod & {
    animation-delay: 3.3s;
  }
  .chart--design & {
    animation-delay: 4.5s;
  }
}

.chart--horiz {
  overflow: hidden;
}

.chart__bar {
  height: 30px;
  margin-bottom: 10px;
  background: linear-gradient(to left, #091b54, #040c26);
  border-top-right-radius: 4px;
  border-bottom-right-radius: 4px;
  opacity: 0;
  -webkit-animation: 1s anim-lightspeed-in ease forwards;
  animation: 1s anim-lightspeed-in ease forwards;
}

.chart__label {
  padding-left: 10px;
  line-height: 30px;
  color: white;
}

//Keyframes
@keyframes anim-lightspeed-in {
  0% {
    transform: translateX(-200%);
    opacity: 1;
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}
</style>