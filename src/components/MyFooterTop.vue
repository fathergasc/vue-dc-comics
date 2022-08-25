<template>
    <div  id="footer_top">
        <div class="container">
            <ul class="product d-flex justify-content-center align-items-center">
                <li v-for="(product, index) in products" :key="index" class="my-5 mx-3 d-flex justify-space-around align-items-center">
                    <a href="product.url">
                        <img class="product-img" :src="require(`../assets/images/${product.image}`)" :alt="product.text">
                        <!-- <img :src="getImage(product.image)"> alternative to print images in a v-for through a method -->
                        <span class="uppercase text-white px-3">{{product.text}}</span>
                    </a>
                    
                </li>
            </ul>
        </div>
    </div>
    
</template>

<script>
export default {
    name: 'MyFooterTop',
    methods: {
        //alternative to print images in a v-for through a method
        /*getImage(path) {
        return require('../assets/images/' + path);
        },*/
    },
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
        background-color: $brand_color;
    }

    .product-img {
        height: 60px;
        max-width: 60px;
    }

    li {
        span {
            font-size: 14px;
        }

        a:hover {
            transform: scale(1.1);
        }
    }
</style>