<script>

export default {
    data(){
        return{
            props:{
                type: Object
            }
        }
    }
}
</script>

<template>
    <div class="col-2">
        <img :src="type.thumb" alt="Comics" class="img-fluid">
    </div>
</template>
<style lang="scss" scoped>
.col-2{
    height: 300px;
    width: 300px;
    
    img{
        height: 100%;
        width: 100%;
    }
}

</style>