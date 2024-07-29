<script>
export default {
    data(){
        return{
            dc_comics:[
                {
                    label: "Characters",
                    url: "#"
                },
                {
                    label: "Comics",
                    url: "#"
                },
                {
                    label: "Movies",
                    url: "#"
                },
                {
                    label: "TV",
                    url: "#"
                },
                {
                    label: "Games",
                    url: "#"
                },
                {
                    label: "Videos",
                    url: "#"
                },
                {
                    label: "News",
                    url: "#"
                },
            ],

            shops:[
                {
                    label: "Shop DC",
                    url: "#"
                },
                {
                    label: "Shop DC collectibles",
                    url: "#"
                }
            ],

            dc:[
                {
                    label: "Terms Of Use",
                    url: "#"
                },
                {
                    label: "Privacy Policy (New)",
                    url: "#"
                },
                {
                    label: "Ad Choices",
                    url: "#"
                },
                {
                    label: "Advertising",
                    url: "#"
                },
                {
                    label: "Jobs",
                    url: "#"
                },
                {
                    label: "Subscriptions",
                    url: "#"
                },
                {
                    label: "Talent Workshops",
                    url: "#"
                },
                {
                    label: "CPSC Certificates",
                    url: "#"
                },
                {
                    label: "Ratings",
                    url: "#"
                },
                {
                    label: "Shop Help",
                    url: "#"
                },
                {
                    label: "Contact Us",
                    url: "#"
                },
            ],

            sites:[
                {
                    label: "DC",
                    url: "#"
                },
                {
                    label: "MAD Magazine",
                    url: "#"
                },
                {
                    label: "DC Kids",
                    url: "#"
                },
                {
                    label: "DC Universe",
                    url: "#"
                },
                {
                    label: "DC Power Visa",
                    url: "#"
                },
            ]

        }
    }
}
</script>
<template>
    <main class="bg-dark">
        <div class="container">
            <div class="row">
                <div class="col-12 py-5">
                    <h2><a href="#" class="text-decoration-none text-light"> --> Content goes here <-- </a></h2>
                </div>
            </div>
        </div>

        <div class="container-full bg-primary blue-section">
            <div class="row">
                <div class="col-2 offset-2">
                    PROVA
                </div>

                <div class="col-2">
                    PROVA
                </div>

                <div class="col-2">
                    PROVA
                </div>

                <div class="col-2">
                    PROVA
                </div>

                <div class="col-2">
                    PROVA
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
</style>