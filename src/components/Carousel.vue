<template>
  <div id="carousel">
    <!-- <img :src="arrows.arrowLeft" class="arrows" @click="gotToPreviousSlide"/> -->
  <div class="carousel-control-prev-icon" @click="gotToPreviousSlide"></div>
    <div id="petBox">
        <h3 id="petName">Meet {{petName}}</h3>
         <img :src="this.singleSlide" width="500px" height="500px" id="image"/>
    </div>
    <!-- <img :src="arrows.arrowRight" class="arrows" @click="goToNextSlide"/> -->
    <div class="carousel-control-next-icon" @click="goToNextSlide"></div>
  </div>
</template>

<script>


export default {
   
    data() {
        return {
            images: [
                {name: require('@/assets/img/bea.jpg'),
                 petName:"Bea"},
                {name: require('@/assets/img/ben.jpg'),
                 petName:"Ben"},
                {name: require('@/assets/img/jasmine.jpg'),
                 petName:"Jasmine"},
                {name: require('@/assets/img/oliver.jpg'),
                 petName:"Oliver"},
            ],
            
            arrows: {
                arrowLeft: require('@/assets/img/arrow-left.png'),
                arrowRight: require('@/assets/img/arrow-right.png'),
            },

            currentImage: "",
            singleSlide: "",
            petName: "",
           
        }
    },

    created() {
         this.currentImage = 0;
         this.singleSlide = this.images[this.currentImage].name;
         this.petName = this.images[this.currentImage].petName;
    },

    methods: {
        goToNextSlide() {
            this.currentImage++;
            let singleImage = this.images[this.currentImage].name;
            this.singleSlide = singleImage;
            this.goToNextPetName();
          
            return this.singleSlide
        },
        gotToPreviousSlide() {
            this.currentImage--;
            let singleImage = this.images[this.currentImage].name;
            this.singleSlide = singleImage;
            console.log("THIS IS THE slide", petName);
            this.goToPreviousPetName();
            return this.singleSlide
        },

        goToNextPetName() {
            let singlePetName = this.images[this.currentImage].petName;
            this.petName = singlePetName;

            return this.petName
        },

         goToPreviousPetName() {
            let singlePetName = this.images[this.currentImage].petName;
            this.petName = singlePetName;
            return this.petName
         }
    }
}
</script>



<style lang="scss">

@import "../styles/global.scss";
@import "../styles/components/carousel.scss";

@import url('https://fonts.googleapis.com/css?family=Gochi+Hand|Itim&display=swap');


</style>


