<template>
    <section :style="{backgroundImage:image}" class="py-5">
            <h1 class="pt-5 fw-bold text-center">{{title}}</h1>
            <p class="text-center">{{desc}} <a class="text-dark" href="#">{{link}}</a></p>
            <div class="btns d-flex flex-md-row flex-column justify-content-center align-items-center pt-5 mt-5">
                <button class="bg-dark text-white">Custom Order</button>
                <button class="bg-light">Existing Inventory</button>
            </div>
    </section>
</template>
<script>
export default {
    name: 'sectionComp',
    props:{
        title: String,
        desc: String,
        link: String,
        image:String
    }, 
}
</script>
<style lang="scss" scoped>
section{
    height: 100vh;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    overflow: hidden;
    // background-attachment: fixed;
    .btns{
        height: 115%;
        button{
        width: 280px;
        padding:.5rem;
        margin: .5rem;
        border: none;
        border-radius: 3px;
    }
    }
}
</style>