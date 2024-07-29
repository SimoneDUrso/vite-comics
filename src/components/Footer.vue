<script>
export default {
    data(){
        return{
            icons:[
                {
                    image: "./src/assets/footer-facebook.png",
                    url: "#"
                },
                {
                    image: "./src/assets/footer-twitter.png",
                    url: "#"
                },
                {
                    image: "./src/assets/footer-youtube.png",
                    url: "#"
                },
                {
                    image: "./src/assets/footer-pinterest.png",
                    url: "#"
                },
                {
                    image: "./src/assets/footer-periscope.png",
                    url: "#"
                },
            ]
        }
    }
}
</script>
<template>
    <footer class="position-relative">
        <div class="container">
            <div class="row">
                <div class="col-12 ps-0 mt-5 d-flex justify-content-between align-items-center fs-5">
                    <button class="btn btn-lg border border-primary text-white">SIGN-UP NOW!</button>
                    <div>
                        <span class="text-primary mx-2 fw-bold">FOLLOW US</span>
                        <span v-for="icon, index in icons" :key="index" class="mx-2"><a href="#"><img :src="icon.image" alt=""></a></span>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>
<style lang="scss" scoped>
    footer{
        background-color: #303030;
        height: 150px;
        z-index: 50;
    }
</style>