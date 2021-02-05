<template>
    <TheNavigation />
    <SlideShow />
</template>

<script>
import TheNavigation from '@/components/TheNavigation.vue'
import SlideShow from '@/components/SlideShow.vue'

export default {
    name: 'App',
    components: {
        TheNavigation,
        SlideShow,
    },
}
</script>

<style lang="scss">
:root {
    --color-primary: #58abda;
}

html {
    font-size: 62.5%;
    @media (max-width: 650px) {
        font-size: 50%;
    }
}

* {
    box-sizing: border-box;
    margin: 0;
}
</style>
