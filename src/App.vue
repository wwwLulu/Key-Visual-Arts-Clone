<template>
    <TheNavigation />
    <SlideShow />
    <div class="main-content">
        <TheArticles />
        <SideBar />
    </div>
</template>

<script>
import TheNavigation from '@/components/TheNavigation.vue'
import SlideShow from '@/components/SlideShow.vue'
import TheArticles from '@/components/TheArticles'
import SideBar from '@/components/SideBar'

export default {
    name: 'App',
    components: {
        TheNavigation,
        SlideShow,
        TheArticles,
        SideBar,
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

body {
    font-family: Meiryo, sans-serif, monospace;
    background: #eaeaea;
}

.main-content {
    padding: 5rem;
    width: 100%;
    display: flex;
    justify-content: center;
    & > div {
        margin: 0 5rem;
    }
    @media (max-width: 1200px) {
        flex-direction: column;
        align-items: center;
    }
    @media (max-width: 650px) {
        padding: 3rem;
    }
}
</style>
