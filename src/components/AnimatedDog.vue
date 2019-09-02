<template>
    <div class="dog-container">
        <p class="dog-title">To play with me, please click on my head or my tail, woof-woof!!</p>
        <div class="animated-dog">
            <img v-bind:class="{ 'animate-head': isDogHeadClicked }" class="dog-head" :src="images.dogHead" @click="animateHead"/>
            <img class="dog-body" :src="images.dogBody"/>
            <img v-bind:class="{ 'animate-tail': isDogTailClicked }" class="dog-tail" :src="images.dogTail" @click="animateTail"/>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isDogHeadClicked: false,
            isDogTailClicked: false,
            images: {
                dogBody: require('@/assets/img/dog-body.png'),
                dogBone: require('@/assets/img/dog-bone.png'),
                dogHead: require('@/assets/img/dog-head.png'),
                dogTail: require('@/assets/img/dog-tail.png')
            }
        }
         
    },
    methods: {
        animateHead() {
            this.isDogHeadClicked = !this.isDogHeadClicked;
        },
        animateTail() {
            this.isDogTailClicked = !this.isDogTailClicked;
        }
    }
}
</script>

<style lang="scss">

@import "../styles/global.scss";
@import "../styles/components/animatedDog.scss";

@import url('https://fonts.googleapis.com/css?family=Gochi+Hand|Itim&display=swap');

</style>