<template>
 <div id="boxes-container">
    <div class="box">
        <span class="text">How to reduce cat allergies without medication</span>
         <img :src="images.cat1" width="200px" height="200px" />
    </div>
    <div class="box">
        <span class="text">How to Know What Your Cat is Thinking</span>
         <img :src="images.cat2" width="200px" height="200px" />
    </div>
     <div class="box">
        <span class="text">Why You Should Adopt a Pet</span>
         <img :src="images.dog" width="200px" height="200px"/>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
               images: {
                cat1: require('@/assets/img/cat1.jpeg'),
                cat2: require('@/assets/img/cat2.jpeg'),
                dog: require('@/assets/img/dog1.png'),
            }
        }
         
    }
}
</script>

<style lang="scss">

@import "../styles/global.scss";
@import "../styles/components/promoBoxes.scss";

@import url('https://fonts.googleapis.com/css?family=Gochi+Hand|Itim&display=swap');

</style>