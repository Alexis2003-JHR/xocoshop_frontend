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
          <img :src="require(`../assets/Home_Gallery/${slide}.png`)" alt="">
        </div>
      </Slide>
    </Carousel>
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
</style>
