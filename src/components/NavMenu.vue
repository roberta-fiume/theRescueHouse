<template>
  <div>
    <div class="icon-container">
        <img :src="images.logo" id="logo"/>
        <img :src="images.menu" id="menu" @click="toggleMenu"/>
        <img :src="images.closeMenu" id="close-menu" v-if="closeMenuIcon"/>
    </div>
    <div class="nav-bar" v-if="navBar">
     <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Adopt</a></li>
      <li><a href="#">How you can help</a></li>
    </div>
 
  </div>
</template>

<script>
export default {
  name: 'NavMenu',

  data() {
    return {
      images: {
        logo: require('@/assets/img/logo.jpg'),
        menu: require('@/assets/img/icon-menu.png'),
        closeMenu: require('@/assets/img/close-menu.png'),
      },
      navBar: false,
      closeMenuIcon: false
    }    
  },

  methods: {
    toggleMenu() {
      this.navBar = !this.navBar
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

  @import "../styles/global.scss";

  @import "../styles/components/navmenu.scss";

  @import url('https://fonts.googleapis.com/css?family=Gochi+Hand|Itim&display=swap');

</style>




