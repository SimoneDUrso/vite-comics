<script>

export default {
    props:{
        comic: Object
    },
    
    data(){
        return{
            
        }
    }
}
</script>

<template>
    <div class="col-2 mx-auto my-4">
        <a href="#" class="text-decoration-none">
            <img :src="comic.thumb" alt="Comics" class="img-fluid">
            <p class="text-white">{{ comic.series }}</p>
        </a>
    </div>
</template>
<style lang="scss" scoped>
.col-2{
    max-width: 200px;
    min-width: 200px;
    aspect-ratio: 1 / 1;
    
    img{
        max-width: 100%;
        min-width: 100%;
        max-height: 100%;
        object-fit: cover;
        object-position: top;
        transition: opacity 0.3s ease;

        &:hover{
            opacity: 0.5;
        }
    }
}

</style>