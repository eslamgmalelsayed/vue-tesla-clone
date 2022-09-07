<template>
    <button>
        <slot name="button"></slot>
    </button>
</template>

<script>
export default {
    name:'buttonComp',
}
</script>

<style lang="scss" scoped>
    button{
    width: 280px;
    padding:.5rem;
    margin: .5rem;
    border: none;
    border-radius: 3px;
    @media(max-width:775px){
        width: 180px;
    }
    }
</style>