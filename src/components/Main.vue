<script>
import { dc_comics, shops, dc, sites, navMain } from '../data/menuLists';
import Hero from './partials/Hero.vue';

export default {
    components:{
        Hero
    },

    data(){
        return{
            dc_comics,
            shops,
            dc,
            sites,
            navMain,
            
        }
    }
}
</script>
<template>
    <main class="bg-dark">
        <Hero />
        <div class="container">
            <div class="row">
                <div class="col-12 py-5">
                    <h2><a href="#" class="text-decoration-none text-light fw-bold"> --> Content goes here <-- </a></h2>
                </div>
            </div>
        </div>

        <div class="container-full bg-primary blue-section">
            <div class="row justify-content-center align-items-center">
                <div class="col-2" v-for="nav, index in navMain">
                    <div class="d-flex justify-content-center align-items-center">
                        <img :src="nav.image" alt="Immagini">
                        <span class="ms-2"><a class="text-decoration-none text-white" :href="nav.url">{{ nav.label }}</a></span>
                    </div>
                </div>
            </div>
        </div>

        <div class="bg-image">

            <div class="container py-5">
                <div class="row">
                    <div class="col-12 d-flex p-0">
                        <div class=" d-flex ">
                            <div class="me-4">
                                    <h4 class="text-white">DC COMICS</h4>
                                <ul class="list-unstyled">
                                    <li v-for="comic, index in dc_comics"><a class="text-decoration-none text-secondary" :href="comic.url">{{ comic.label }}</a></li>
                                </ul>
    
                                <h4 class="text-white">SHOP</h4>
                                <ul class="list-unstyled">
                                    <li v-for="shop, index in shops"><a class="text-decoration-none text-secondary" :href="shop.url">{{shop.label}}</a></li>
                                </ul>
                            </div>
    
                            <div class="mx-4">
                                <h4 class="text-white">DC</h4>
                                
                                <ul class="list-unstyled">
                                    <li v-for="dc, index in dc"><a class="text-decoration-none text-secondary" href="dc.url">{{dc.label}}</a></li>
                                </ul>
                            </div>
    
                            <div class="mx-4">
                                <h4 class="text-white">SITES</h4>
                                <ul class="list-unstyled">
                                    <li v-for="site, index in sites"><a class="text-decoration-none text-secondary" href="site.url">{{site.label}}</a></li>
                                </ul>
                            </div>
    
                            <div class="dc-logo-bg position-relative">
                                <img class="position-absolute img-fluid" src="../assets/dc-logo-bg.png" alt="">
                            </div>
                        </div>
    
                        
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>
<style lang="scss" scoped>
    .blue-section{
        padding: 60px 0px;
        position: relative;
        z-index: 50;
        overflow-x: hidden;
    }

    .bg-image{
        background-image: url(../assets/footer-bg.jpg);
        background-size: cover;
        min-height: 460px;
    }

    .dc-logo-bg{
        top: -80px;
        left: 200px;
        width: 1000px;
    }

    .col-2{
        width: 13%;
        span{
            font-size: 14px;
        }

        img{
            width: 50px;
            height: 65px;
            object-fit: contain;
        }
    }
</style>