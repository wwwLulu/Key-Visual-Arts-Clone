<template>
    <div class="side-bar">
        <img src="@/assets/key_side_banner_vafes.jpg" alt="thumbnail" />
        <img src="@/assets/key_side_banner_primadoll.jpg" alt="thumbnail" />
        <img src="@/assets/key_side_banner_kinenove.jpg" alt="thumbnail" />
        <img src="@/assets/key_side_banner_sprb.jpg" alt="thumbnail" />
        <img src="@/assets/key_side_banner_vafes.jpg" alt="thumbnail" />
        <img src="@/assets//key_kamisama_side_banner.jpg" alt="thumbnail" />
    </div>
</template>

<style lang="scss" scoped>
.side-bar {
    width: 30em;

    margin-top: 2.5rem;
    img {
        width: 100%;
        border-radius: 1rem;
        border: 2px solid white;
        margin-bottom: 5rem;
    }
    @media (max-width: 1200px) {
        width: 100%;
        display: grid;
        gap: 1rem;
        grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    }
}
</style>
