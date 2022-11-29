<template>
  <div class="home">
    <Slide/>
  </div>
</template>

<script>
// @ is an alias to /src
import Slide from "../components/Slide.vue"

export default {
  name: 'HomeView',
  components: {
    Slide,
  },
}
</script>

<style>
.home{
  height: 100%;
  width: 100%;
}
</style>
