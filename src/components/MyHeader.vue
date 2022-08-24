<template>
    <header class="container d-flex justify-content-between align-items-center">
        <img src="@/assets/images/dc-logo.png" alt="DC Logo">
        <ul class="">
            <li class="d-inline-block mx-3" v-for="(link, index) in nav_links" :key="index" :class="(link.active == true)?'active':''">
                <a href="link.url" :class="(link.active == true)?'active':''">{{link.text}}</a>
            </li>
        </ul>
    </header>
</template>

<script>
export default {
    name: 'MyHeader',
    data() {
        return {
            nav_links: [
                {
                    text: 'characters',
                    url: '#',
                    active: false,
                },
                {
                    text: 'comics',
                    url: '#',
                    active: true,
                },
                {
                    text: 'movies',
                    url: '#',
                    active: false,
                },
                {
                    text: 'tv',
                    url: '#',
                    active: false,
                },
                {
                    text: 'games',
                    url: '#',
                    active: false,
                },
                {
                    text: 'collectibles',
                    url: '#',
                    active: false,
                },
                {
                    text: 'videos',
                    url: '#',
                    active: false,
                },
                {
                    text: 'fans',
                    url: '#',
                    active: false,
                },
                {
                    text: 'news',
                    url: '#',
                    active: false,
                },
                {
                    text: 'shop',
                    url: '#',
                    active: false,
                },
            ]}
        }
    }
    
</script>

<style scoped lang="scss">

@import '../styles/vars.scss';

    header {
        height: 120px;
        background-color: white;
    }

    img {
        height: 70%;
    }

    ul {
        margin-bottom: 0; // bootstrap puts 1rem as margin-bottom on ul
    }

    li {
        position: relative;
    }
    li.active:after {
            content: '';
            position: absolute;
            display: block;
            bottom: 0;
            right: 0;
            width: 100%;
            height: 5px;
            background-color: $brand_color;
        }

    a {
        line-height: 120px;
        height: 100%;
        font-size: 13px;
        text-transform: uppercase;
        color: $black;
        font-weight: bold;
        position: relative;

        
        &.active, &:hover {
            color: $brand_color;
        }

        

    }



</style>