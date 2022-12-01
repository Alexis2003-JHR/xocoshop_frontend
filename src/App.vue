<template>
  <div class="app">
    <Nav/>
    <router-view/>
  </div>
</template>

<script>
import Nav from "./components/Nav-bar.vue";

export default{
  name: "App",
  components:{
    Nav
  }
}
</script>

<style>
/*Allan & Nunito font*/
@import url('https://fonts.googleapis.com/css2?family=Allan:wght@400;700&family=Nunito:ital,wght@0,300;0,400;0,500;0,700;1,300&display=swap');

* {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>