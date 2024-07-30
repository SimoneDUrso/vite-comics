<script>
import { navItems } from '../data/menuLists';

export default {
    data(){
        return{
            navItems
        }
    }
}
</script>
<template>
    <header>
        <div class="container mt-2">
            <div class="row">
                <div class="col-12 d-flex align-items-center justify-content-between ">
                    <img src="../assets/dc-logo.png" alt="" class="mb-2">
                    <ul class="list-unstyled d-flex">
                        <li v-for="item, index in navItems" :key="index" class="px-2"><a class="text-decoration-none " :href="item.url" :class="item.clicked ? 'active' : '' ">{{ item.label }}</a></li>
                    </ul>
                </div>
            </div>
        </div>
    </header>
</template>
<style lang="scss" scoped>
    ul{
        li{
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            a{
                color: black;
                transition: color 0.2s ease;

                &:hover{
                    color: rgb(12, 124, 236);
                }
            }

            .active{
                border-bottom: 5px solid rgb(12, 124, 236);
                padding-bottom: 50px;
                color: rgb(12, 124, 236);
            }
        }
    }
    
</style>