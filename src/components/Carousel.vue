<template>
  <div id="carousel">
    <img :src="arrows.arrowLeft" class="arrows" @click="gotToPreviousSlide"/>
    <img :src="this.singleSlide" width="500px" height="500px" id="image"/>
    <img :src="arrows.arrowRight" class="arrows" @click="goToNextSlide"/>
  </div>
</template>

<script>
//  import mediaQueries from '../_mediaQueries.scss'


export default {
   
    data() {
        return {
            images: [
                {name: require('@/assets/img/bea.jpg')},
                {name: require('@/assets/img/ben.jpg')},
                {name: require('@/assets/img/jasmine.jpg')},
                {name: require('@/assets/img/oliver.jpg')},
            ],
            
            arrows: {
                arrowLeft: require('@/assets/img/arrow-left.png'),
                arrowRight: require('@/assets/img/arrow-right.png'),
            },

            currentImage: "",
            singleSlide: ""
           
        }
    },

    created() {
         this.currentImage = 0;
         this.singleSlide = this.images[this.currentImage].name;
    },

    methods: {
        goToNextSlide() {
            this.currentImage++;
            // console.log("CURRENT IMAGE", this.currentImage)
            let singleImage = this.images[this.currentImage].name;
                // console.log("imageeee", singleImage)
            this.singleSlide = singleImage;
            // console.log("slideeeeee", this.singleSlide)
            return this.singleSlide
        },
        gotToPreviousSlide() {
            this.currentImage--;
            let singleImage = this.images[this.currentImage].name;
            this.singleSlide = singleImage;
            return this.singleSlide
        }
    }
}
</script>



<style lang="scss">

@import "../styles/global.scss";
@import "../styles/components/carousel.scss";

    // @media only screen and (min-width: 768px) {

    // }

    // @media only screen and (min-width: 1024px) {

    // }


</style>


