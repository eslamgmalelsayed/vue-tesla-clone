<template>
    <section @click="hideSideBar" :style="{backgroundImage:image}" class="py-5" :id="id">
            <h1 class="pt-5 fw-bold text-center">{{title}}</h1>
            <p class="text-center">{{desc}} <a class="text-dark" href="#">{{link}}</a></p>
            <div class="btns d-flex flex-md-row flex-column justify-content-center align-items-center pt-5 mt-5">
                <!-- button -->
                <buttonComp class="bg-dark text-white">
                    <template #button>
                        Custom Order   
                    </template>
                </buttonComp>
                <buttonComp class="bg-light">
                <template #button>
                    Existing Inventory  
                </template>
                </buttonComp>
            </div>
    </section>

</template>
<script>
// imports
import buttonComp from '../buttonComp.vue'
export default {
    name: 'sectionComp',
    components:{
        buttonComp
    },
    props:{
        title: String,
        desc: String,
        link: String,
        image:String,
        hideSideBar:Function,
    },
}
</script>
<style lang="scss" scoped>
section{
    position: relative;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
    overflow: hidden;
    height: 100vh;
    .btns{
        height: 115%;
    }
}
</style>