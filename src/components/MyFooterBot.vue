<template>
    <footer>
            <div class="footer_top">
                <div class="container d-flex justify-content-between">
                    <div class="lists pt-5 pb-3 d-flex flex-column align-content-start flex-wrap">
                    <ul>
                        <span class="fs-5 fw-bold text-white">DC COMICS</span>
                        <li v-for="(link, index) in dc_comics_links" :key="index">
                            <a href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                    <ul>
                        <span class="fs-5 fw-bold text-white">SHOP</span>
                        <li v-for="(link, index) in shop_links" :key="index">
                            <a href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                    <ul>
                        <span class="fs-5 fw-bold text-white">DC</span>
                        <li v-for="(link, index) in dc_links" :key="index">
                            <a href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                    <ul>
                        <span class="fs-5 fw-bold text-white">SITES</span>
                        <li v-for="(link, index) in sites_links" :key="index">
                            <a href="link.url">{{link.text}}</a>
                        </li>
                    </ul>
                </div>
                <div class="big-logo-footer">
                </div>
                </div>
                
                
            </div>
            
            <div class="footer_bot">
                <div class="container d-flex justify-content-between align-items-center p-5">
                    <div class="footer_bot_l">
                        <a href="#"><span id="sign-up">SIGN UP NOW!</span></a>
                    </div>
                    <div class="footer_bot_r d-flex justify-content-between align-items-center">
                        <span class="fs-5 fw-bold" id="follow">FOLLOW US</span>
                        <ul class="contacts-list d-flex justify-content-between align-items-center">
                            <li v-for="(contact, index) in contacts_links" :key="index" class="px-2 scaleonhover">
                                <a :href="contact.url">
                                    <img :src="require(`../assets/images/${contact.image}`)" :alt="contact.text">
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
                
            </div>  
    </footer>
</template>

<script>
export default {
    name: 'MyFooterBot',
    data() {
        return {
            dc_comics_links: [
                {
                    text: 'Characters',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Comics',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Movies',
                    url: '#',
                    active: false,
                },
                {
                    text: 'TV',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Games',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Videos',
                    url: '#',
                    active: false,
                },
                {
                    text: 'News',
                    url: '#',
                    active: false,
                },
            ],
            shop_links: [
                {
                    text: 'Shop DC',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Shop DC Collectibles',
                    url: '#',
                    active: false,
                },
            
            ],
            dc_links: [
                {
                    text: 'Terms Of Use',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Privacy policy (New)',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Ad Choices',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Advertising',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Jobs',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Subscriptions',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Talent Workshops',
                    url: '#',
                    active: false,
                },
                {
                    text: 'CPSC Certificates',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Ratings',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Shop Help',
                    url: '#',
                    active: false,
                },
                {
                    text: 'Contact Us',
                    url: '#',
                    active: false,
                },
            ],
            sites_links: [
                {
                    text: 'DC',
                    url: '#',
                    active: false,
                },
                {
                    text: 'MAD MAgazine',
                    url: '#',
                    active: false,
                },
                {
                    text: 'DC Kids',
                    url: '#',
                    active: false,
                },
                {
                    text: 'DC Universe',
                    url: '#',
                    active: false,
                },
                {
                    text: 'DC Power Visa',
                    url: '#',
                    active: false,
                },
            ],
            contacts_links: [
                {
                    text: 'Facebook',
                    image: 'footer-facebook.png',
                    url: '#',
                },
                {
                    text: 'Twitter',
                    image: 'footer-twitter.png',
                    url: '#',
                },
                {
                    text: 'Youtube',
                    image: 'footer-youtube.png',
                    url: '#',
                },
                {
                    text: 'Pinterest',
                    image: 'footer-pinterest.png',
                    url: '#',
                },
                {
                    text: 'Periscope',
                    image: 'footer-periscope.png',
                    url: '#',
                },
                
            ]
        }
    }
}

</script>

<style scoped lang="scss">
    @import '../styles/vars.scss';

    ul {
        margin-bottom: 1rem;
        li a {
            color: rgb(204, 199, 199);
        }
    }

    li:hover {
        a {
            color: white;
        }
    }

    .footer_top {
        height: 400px;
        width: 100%;
        background-image: url(../assets/images/footer-bg.jpg);
        background-size: contain;
        background-position: center;

        .container {
            height: 100%;
        }
    }

    .lists {
        height: 100%;
    }

    .big-logo-footer {
        height: 400px;
        width: 500px;
        background-image: url(../assets/images/dc-logo-bg.png);
        background-size: cover;
        background-position: center;
    }

    .footer_bot {
        background-color: #303030;
        z-index: 1;
    }

    #sign-up {
        color: white;
        outline: 3px solid $brand_color;
        padding: 0.7rem;

        &:hover {
            background-color: $brand_color;
        }
    }

    #follow {
        color: #0282f9;
    }

    .contacts-list {
        margin-bottom: 0;
    }

    .scaleonhover:hover {
        transform: scale(1.1);
    }
</style>