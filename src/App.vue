<template>
  <div id="app">
    <NavMenu />
    <Carousel />
    <PromoBoxes />
    <AnimatedDog />
    <Footer />
  </div>
</template>

<script>
import NavMenu  from './components/NavMenu.vue'
import Carousel from './components/Carousel.vue'
import PromoBoxes from './components/PromoBoxes.vue'
import AnimatedDog from './components/AnimatedDog.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'app',
  components: {
    NavMenu ,
    Carousel,
    PromoBoxes,
    AnimatedDog,
    Footer
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
body {
  margin: 0;
}
</style>
