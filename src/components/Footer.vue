<script>
import { icons } from '../data/menuLists';

export default {
    data(){
        return{
            icons
        }
    }
}
</script>
<template>
    <footer class="position-relative">
        <div class="container">
            <div class="row">
                <div class="col-12 ps-0 mt-5 d-flex justify-content-between align-items-center fs-5">
                    <button class="btn btn-lg border border-primary">SIGN-UP NOW!</button>
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

        button{
            color: white;
            transition: background-color 0.4s ease;
            transition: color 0.3s ease;
            

            &:hover{
                background-color: gray;
                color: black;
            }
        }

        img{
            transition: opacity 0.2s ease;

            &:hover{
                opacity: 0.3;
            }
        }
    }
</style>