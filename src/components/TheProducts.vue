<template>
    <section class="products">
        <div class="products__header">
            <div class="line"></div>
            <h3 class="products__title">Products</h3>
            <div class="line"></div>
        </div>
        <div class="products__gallery">
            <div class="products__product">
                <div class="products__product--overlay"></div>
                <img src="@/assets/product_image_kamisama.jpg" alt="product" />
                <p>Visit</p>
            </div>
            <div class="products__product">
                <div class="products__product--overlay"></div>
                <img src="@/assets/product_image_sprb.jpg" alt="product" />
                <p>Visit</p>
            </div>
            <div class="products__product">
                <div class="products__product--overlay"></div>
                <img src="@/assets/product_image_sp.jpg" alt="product" />
                <p>Visit</p>
            </div>
            <div class="products__product">
                <div class="products__product--overlay"></div>
                <img src="@/assets/product_image_charlotte.jpg" alt="product" />
                <p>Visit</p>
            </div>
            <div class="products__product">
                <div class="products__product--overlay"></div>
                <img src="@/assets/product_image_ab1st.jpg" alt="product" />
                <p>Visit</p>
            </div>
            <div class="products__product">
                <div class="products__product--overlay"></div>
                <img src="@/assets/product_image_rewritehf.jpg" alt="product" />
                <p>Visit</p>
            </div>
            <div class="products__product">
                <div class="products__product--overlay"></div>
                <img src="@/assets/product_image_kudwaf.jpg" alt="product" />
                <p>Visit</p>
            </div>
            <div class="products__product">
                <div class="products__product--overlay"></div>
                <img src="@/assets/product_image_rewritehf.jpg" alt="product" />
                <p>Visit</p>
            </div>
            <div class="products__product">
                <div class="products__product--overlay"></div>
                <img
                    src="@/assets/product_image_planetarian.jpg"
                    alt="product"
                />
                <p>Visit</p>
            </div>
            <div class="products__product">
                <div class="products__product--overlay"></div>
                <img src="@/assets/product_image_clannad.jpg" alt="product" />
                <p>Visit</p>
            </div>
            <div class="products__product">
                <div class="products__product--overlay"></div>
                <img src="@/assets/product_image_kanon.jpg" alt="product" />
                <p>Visit</p>
            </div>
        </div>
    </section>
</template>
<style lang="scss" scoped>
.line {
    width: 10rem;
    height: 0.2rem;
    background: white;
}
.products {
    width: 100%;
    height: 100%;
    padding: 5rem;
    background: #4e4e5c;
    &__header {
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-bottom: 5rem;
    }
    &__title {
        margin: 0 2rem;
        font-size: 2.4rem;
        color: white;
    }
    &__gallery {
        width: 100%;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(30rem, 1fr));
        gap: 2rem;
        @media (max-width: 800px) {
            grid-template-columns: 1fr 1fr;
        }
    }
    &__product {
        position: relative;
        border-radius: 2rem;
        overflow: hidden;
        img {
            border-radius: inherit;
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: center;
        }
        p {
            display: none;
            z-index: 5000;
            position: absolute;
            font-size: 2.4rem;
            color: white;
            top: 1rem;
            left: 0;
            width: 100%;
            text-align: center;
        }
        &:hover &--overlay {
            z-index: 4000;
            cursor: pointer;
            position: absolute;
            border-radius: inherit;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.2);
        }
        &:hover {
            img {
                filter: blur(5px);
            }
        }
        &:hover p {
            display: inline-block;
        }
    }
}
</style>
