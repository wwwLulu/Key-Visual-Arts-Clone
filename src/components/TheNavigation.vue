<template>
    <div class="nav">
        <div class="nav__left">
            <img class="nav__logo" src="../assets/header_logo.png" />
            <nav class="nav__links">
                <img
                    class="nav__link"
                    @mouseenter="newsIcon = 'header_news_icon_a.png'"
                    @mouseleave="newsIcon = 'header_news_icon.png'"
                    :src="require('../assets/' + newsIcon)"
                    alt="News"
                />
                <img
                    class="nav__link"
                    @mouseenter="productIcon = 'header_product_icon_a.png'"
                    @mouseleave="productIcon = 'header_product_icon.png'"
                    :src="require('../assets/' + productIcon)"
                    alt="Products"
                />
                <img
                    class="nav__link"
                    @mouseenter="blogIcon = 'header_blog_icon_a.png'"
                    @mouseleave="blogIcon = 'header_blog_icon.png'"
                    :src="require('../assets/' + blogIcon)"
                    alt="Blog"
                />
                <img
                    class="nav__link"
                    @mouseenter="shopIcon = 'header_shop_icon_a.png'"
                    @mouseleave="shopIcon = 'header_shop_icon.png'"
                    :src="require('../assets/' + shopIcon)"
                    alt="Shop"
                />
            </nav>
        </div>

        <div class="nav__right">
            <div class="nav__social-icons">
                <img
                    class="nav__social-icon"
                    src="../assets/sns_twitter_bt.png"
                    alt="twitter"
                />
                <img
                    class="nav__social-icon"
                    src="../assets/sns_facebook_bt.png"
                    alt="facebook"
                />
                <img
                    class="nav__social-icon"
                    src="../assets/sns_youtube_bt.png"
                    alt="youtube"
                />
            </div>
            <img
                class="nav__mascot"
                src="../assets/header_inari.png"
                alt="mascot"
            />
        </div>

        <div class="nav__hamburger-menu">
            <div></div>
            <div></div>
            <div></div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            newsIcon: 'header_news_icon.png',
            productIcon: 'header_product_icon.png',
            blogIcon: 'header_blog_icon.png',
            shopIcon: 'header_shop_icon.png',
        }
    },
}
</script>

<style lang="scss" scoped>
.nav {
    display: flex;
    justify-content: space-between;
    padding: 0rem 5rem;
    width: 100%;
    height: 6rem;
    border-top: 0.2rem solid var(--color-primary);
    border-bottom: 0.2rem solid #333;
    &__hamburger-menu {
        display: none;
    }
    &__left {
        display: flex;
        align-items: center;
    }
    &__right {
        display: flex;
        align-items: center;
    }
    &__logo {
        height: 4rem;
    }
    &__links {
        display: flex;
    }
    &__link {
        height: 4rem;
        margin: 0 3rem;
        cursor: pointer;
        padding: 0.5rem 0;
        // &:hover {
        //     border-bottom: 0.2rem solid var(--color-primary);
        // }
    }
    &__social-icon {
        height: 3rem;
        margin: 0 0.5rem;
        &:hover {
            cursor: pointer;
        }
    }
    &__mascot {
        height: 100%;
        margin-left: 1rem;
    }
    @media (max-width: 1375px) {
        height: 100%;
        min-height: 6rem;

        &__right {
            display: none;
        }
    }
    @media (max-width: 1040px) {
        &__left {
            flex-direction: column;
            align-items: flex-start;
        }
        &__logo {
            margin-top: 1rem;
        }
        &__links {
            margin-top: 1rem;
        }
        &__link:first-child {
            margin: 0;
        }
    }
    @media (max-width: 680px) {
        padding: 0;
        justify-content: center;
        align-items: center;
        &logo {
            height: 3rem;
        }
        &__links {
            display: none;
        }
        &__hamburger-menu {
            padding: 0.5rem;
            display: block;
            position: absolute;
            right: 2rem;
            &:hover {
                cursor: pointer;
            }
            div {
                background: #333;
                margin: 0.7rem 0;
                width: 3rem;
                height: 0.3rem;
                border-radius: 0.5rem;
            }
            div:nth-child(1) {
                margin-top: 0;
            }
            div:nth-child(3) {
                margin-bottom: 0;
            }
        }
    }
}
</style>
