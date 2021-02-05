<template>
    <div class="slideshow">
        <h1>hello world</h1>
        <div class="slideshow__background">
            <img :src="require('../assets/' + currentImage)" alt="thumbnail" />
            <div class="blur"></div>
        </div>
        <div class="slideshow__spotlight">
            <img :src="require('../assets/' + currentImage)" alt="thumbnail" />
        </div>
    </div>
</template>

<script>
export default {
    mounted() {
        alert('loaded up')
    },
    data() {
        return {
            currentImage: '',
        }
    },
}
</script>

<style lang="scss" scoped>
.slideshow {
    &__background {
        width: 100vw;
        height: 60rem;
        background: red;
    }
}
</style>
