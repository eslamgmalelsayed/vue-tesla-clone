<template>
    <nav class="fixed-top">
        <div class="container-fluid d-flex justify-content-between align-items-center">
            <div class="logo">
                <a href="#">
                <img src="../../assets/images/tesla.webp" alt="logo" width="140" height="40">
                </a>
            </div>
            <div class="links d-xl-block d-none">             
                <a href="#">Model S</a>
                <a href="#">Model 3</a>
                <a href="#">Model x</a>
                <a href="#">Model y</a>
                <a href="#">Solar Roof</a>
                <a href="#">Solar panels</a>
            </div>
            <div class="end">
                <a class="d-xl-inline d-none" href="#">Shop</a>
                <a class="d-xl-inline d-none" href="#">Account</a>
                <a class="end-link" @click="toggler" href="#">Menu</a>
            </div>
        </div>
    </nav>
</template>
<script>
export default {
    name:'navBar',
    props:{
        show: Boolean,
        toggler:Function
    },
}
</script>
<style lang="scss" scoped>

nav{
    z-index: 999;
    .links a,.end a{
        font-size: .9rem;
        color: #000;
        font-weight: bold;
        text-decoration: none;
        padding: .4rem 1rem;
        transition: .4s;
        border-radius: 3px;
        &:hover{
            color: #000;
            background: rgba(176, 173, 173, 0.3);
        }
    }
    @media(max-width:1200px){
        .end-link{
        background: rgba(176, 173, 173, 0.3);
        }
    }
    img{
        object-fit: cover;
        object-position: center;
    }
}
</style>