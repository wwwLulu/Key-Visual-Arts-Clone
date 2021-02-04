<template>
    <the-navigation></the-navigation>
</template>

<script>
import TheNavigation from '@/components/TheNavigation.vue'

export default {
    name: 'App',
    components: {
        TheNavigation,
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
        font-size: 55%;
    }
}

* {
    box-sizing: border-box;
    margin: 0;
}
</style>
