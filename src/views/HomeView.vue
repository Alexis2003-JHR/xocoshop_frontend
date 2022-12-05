<template>
  <div class="home">
    <Carousel
    :navigation="false"
    :pagination="false"
    :timeout="5000"
    class="carousel"
    v-slot="{currentSlide}">
      <Slide v-for="(slide, index) in carouselSlides" :key="index">
        <div v-show="(currentSlide === index + 1)" class="slide-info">
          <img :src="require(`../assets/Home_assets/Home_Gallery/${slide}.png`)" alt="">
        </div>
      </Slide>
    </Carousel>

    <div class="menu-section">
      <h1>MENÚ</h1>
      <div class="targets">
        <div class="target tgt-1">
          <img src="@/assets/Home_assets/Menu_section/1.Menu.png" alt="">
        </div>

        <div class="target tgt-2">
          <img src="@/assets/Home_assets/Menu_section/2.Menu.png" alt="">
        </div>

        <div class="target tgt-3">
          <img src="@/assets/Home_assets/Menu_section/3.Menu.png" alt="">
        </div>

        <div class="target tgt-4">
          <img src="@/assets/Home_assets/Menu_section/4.Menu.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Carousel from "../components/Carousel.vue"
import Slide from "../components/Slide.vue"

export default {
  name: 'HomeView',
  components: {
    Carousel,
    Slide
  },
  setup(){
    const carouselSlides = ["1.Home-Slider", "2.Home-Slider", "3.Home-Slider", "4.Home-Slider"];

    return {carouselSlides};
  }
}
</script>

<style>
.home{
  position: relative;
  width: 100%;
}
/*SliderGalery*/
.carousel{
  position: relative;
  max-height: 100vh;
  height: 100vh;
}
.slide-info{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  max-height: 100%;
  height: 100%;
}
.carousel img{
  min-width: 100%;
  height: 100%;
  object-fit: cover;
}
/*Main info*/
.inicio-info{
  display: flex;
  flex-wrap: wrap;
  text-align: center;
  justify-content: space-around;
}
.inicio-info h1{
  width: 100%;
  font-weight: 400;
}
.inicio-info img{
  max-width: 100%;
  margin: 50px 0;
}
/*MENÚ SECTION*/
.menu-section{
  position: relative;
  width: 100%;
}
.menu-section h1{
  font-family: 'Allan', cursive;
  font-size: 40px;
  color: #000;
  margin: 30px 0;
}
.targets{
  max-width: 100%;
  widows: 100%;
  height: 86vh;

  /*Grid position*/
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  grid-gap: 10px;
  grid-auto-rows: 100px;
  grid-template-areas: 
  "a a a a z b b b b"
  "a a a a z b b b b"
  "c c c c z d d d d"
  "c c c c z d d d d";
}
.target{
  position: absolute;
}
.tgt-1{
  top: 130px;
  z-index: 1;
  grid-area: z;
  background-color: antiquewhite;
}
.tgt-1 img{
  width: 314px;
  height: 466px;
}
.tgt-2 img, .tgt-2{
  width: 288px;
  height: 387px;
}
.tgt-3 img, .tgt-3{
  width: 308px;
  height: 387px;
}
.tgt-4 img, .tgt-4{
  width: 362px;
  height: 300px;
}
</style>