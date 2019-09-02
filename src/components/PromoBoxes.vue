<template>
 <div id="boxes-container">
    <div class="box" id="box1">
        <span class="text">How to reduce cat allergies without medication</span>
         <img :src="images.cat1"/>
    </div>
    <div class="box" id="box2">
        <span class="text">How to Know What Your Cat is Thinking</span>
         <img :src="images.cat2"/>
    </div>
     <div class="box" id="box3">
        <span class="text">Why You Should Adopt a Pet</span>
         <img :src="images.dog"/>
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