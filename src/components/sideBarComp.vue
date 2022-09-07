<template>
    <div v-show="show" class="side  animate__animated animate__fadeInRight">
        <div class="container py-5 d-flex justify-content-center flex-column">
        <span @click="toggler" role="button" class="text-end pb-4 pe-4 fw-bold fs-5">x</span>
        <a href="#">Existing Inventory</a>
        <a href="#">Used Inventory</a>
        <a href="#">Trade-In</a>
        <a href="#">Test Drive</a>
        <a href="#">Roadster</a>
        <a href="#">Semi</a>
        <a href="#">Existing Inventory</a>
        <a href="#">Used Inventory</a>
        <a href="#">Trade-In</a>
        <a href="#">Test Drive</a>
        </div>
    </div>
</template>

<script>
export default {
    name:"sideBarComp",
    props:{
        show: Boolean,
        toggler:Function,
    },
}
</script>

<style lang="scss" scoped>
.side{
    position: fixed;
    background: #fff;
    right: 0;
    top: 0;
    width: 20%;
    min-width: fit-content;
    height: 100%;
    z-index: 1020;
    a{
        font-size: .9rem;
        padding:.5rem 1.5rem;
        color: #000;
        text-decoration: none;
        font-weight: bold;
    }
}
</style>