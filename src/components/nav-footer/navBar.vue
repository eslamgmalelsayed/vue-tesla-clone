<template>
    <nav class="navbar navbar-expand-lg pt-0 fixed-top d-lg-block d-none">
        <div class="container-fluid">
            <a class="navbar-brand pt-0" href="#">
                <img class="img-fluidd" src="../../assets/images/tesla.webp" alt="logo" width="140" height="50">
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarText" aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarText">
            <ul class="navbar-nav m-auto mb-2 mb-lg-0">
                <li class="nav-item">
                <a class="nav-link" href="#">Model S</a>
                </li>
                <li class="nav-item">
                <a class="nav-link" href="#">Model 3</a>
                </li>
                <li class="nav-item">
                <a class="nav-link" href="#">Model X</a>
                </li>
                <li class="nav-item">
                <a class="nav-link" href="#">Model Y</a>
                </li>
                <li class="nav-item">
                <a class="nav-link" href="#">Solar Roof</a>
                </li>
                 <li class="nav-item">
                <a class="nav-link" href="#">Solar Panels</a>
                </li>
            </ul>
            <span class="navbar-text">
                <a class="text-decoration-none" href="#">shop</a>
                <a class="text-decoration-none px-4" href="#">account</a>
                <a class="text-decoration-none" href="#">menu</a>
            </span>
            </div>
        </div>
    </nav>
</template>
<style lang="scss" scoped>

nav{
    z-index: 999;
    a{
        font-size: .9rem;
        color: #000;
        font-weight: bold;
        &:hover{
            color: #000;
        }
    }
    img{
        object-fit: cover;
        object-position: center;
    }
}
</style>