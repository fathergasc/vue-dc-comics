<template>
    <div  id="footer_top">
        <div class="container">
            <div v-for="(product, index) in products" class="product d-flex justify-content-center align-items-center" :key="index">
                <img :src="'@/assets/images/' + product.image" :alt="product.text">
                
            </div>
        </div>
    </div>
    
</template>

<script>
export default {
    name: 'MyFooterTop',
    data() {
        return {
            products: [
                {
                    text: 'digital comics',
                    url: '#',
                    active: false,
                    image: 'buy-comics-digital-comics.png',
                },
                {
                    text: 'dc merchandise',
                    url: '#',
                    active: false,
                    image: 'buy-comics-merchandise.png',
                },
                {
                    text: 'subscription',
                    url: '#',
                    active: false,
                    image: 'buy-comics-subscriptions.png',
                },
                {
                    text: 'comic shop locator',
                    url: '#',
                    active: false,
                    image: 'buy-comics-shop-locator.png',
                },
                {
                    text: 'dc power visa',
                    url: '#',
                    active: false,
                    image: 'buy-dc-power-visa.svg',
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">

    @import '../styles/vars.scss';

    #footer_top {
        height: 100px;
        background-color: $brand_color;
    }
</style>