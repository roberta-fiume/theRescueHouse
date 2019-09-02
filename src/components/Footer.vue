<template>
    <div class="links">
        <div class="link-box" id="primary-box">
            <li><a href="#">Privacy</a></li>
            <li><a href="#">Returns</a></li>
            <li><a href="#">Terms</a></li>
        </div>
        <div class="link-box" id="secundary-link-box" >
            <a href="#">Copyright</a>
            <div class="social-container">
                <a href="#"><img :src="images.fb" class="social-icon"/></a>
                <a href="#"><img :src="images.twitter" class="social-icon"/></a>
            </div>
   
        </div>
    </div>

    
</template>

<script>
export default {
        data() {
            return {
                images: {
                    fb: require('@/assets/img/fb.png'),
                    twitter: require('@/assets/img/twitter.png'),
                }
            }
    }
}
</script>

<style lang="scss">
    @import "../styles/global.scss";
    @import "../styles/components/footer.scss";
    @import url('https://fonts.googleapis.com/css?family=Gochi+Hand|Itim&display=swap');
</style>