<script>
export default {
    name: "AppFooter",
    data() {
        return {

            links: {
                "DC COMICS": [
                    {
                        name: "Characters",
                        url: "#"
                    },
                    {
                        name: "Comics",
                        url: "#"
                    },
                    {
                        name: "Movies",
                        url: "#"
                    },
                    {
                        name: "TV",
                        url: "#"
                    },
                    {
                        name: "Games",
                        url: "#"
                    },
                    {
                        name: "Videos",
                        url: "#"
                    },
                    {
                        name: "News",
                        url: "#"
                    }
                ],
                "DC": [
                    {
                        name: "Terms Of Use",
                        url: "#"
                    },
                    {
                        name: "Privacy policy(New)",
                        url: "#"
                    },
                    {
                        name: "Ad Choices",
                        url: "#"
                    },
                    {
                        name: "Advertising",
                        url: "#"
                    },
                    {
                        name: "Jobs",
                        url: "#"
                    },
                    {
                        name: "Subscriptions",
                        url: "#"
                    },
                    {
                        name: "Talet Workshops",
                        url: "#"
                    },
                    {
                        name: "CPSC Certificates",
                        url: "#"
                    },
                    {
                        name: "Ratings",
                        url: "#"
                    },
                    {
                        name: "Shop Help",
                        url: "#"
                    },
                    {
                        name: "Contact Us",
                        url: "#"
                    }
                ],
                "SITES": [
                    {
                        name: "DC",
                        url: "#"
                    },
                    {
                        name: "MAD Magazine",
                        url: "#"
                    },
                    {
                        name: "DC Kids",
                        url: "#"
                    },
                    {
                        name: "DC Universe",
                        url: "#"
                    },
                    {
                        name: "DC Power Visa",
                        url: "#"
                    },
                ],
                "SHOP": [
                    {
                        name: "Shop DC",
                        url: "#"
                    },
                    {
                        name: "Shop DC Collectibles",
                        url: "#"
                    }
                ],
            },
            icons: [
                {
                    img: "footer-facebook.png",
                    url: "https://it-it.facebook.com"
                },
                {
                    img: "footer-twitter.png",
                    url: "https://twitter.com/?lang=it"
                },
                {
                    img: "footer-youtube.png",
                    url: "https://www.youtube.com"
                },
                {
                    img: "footer-pinterest.png",
                    url: "https://www.pinterest.it"
                },
                {
                    img: "footer-periscope.png",
                    url: "#"
                },
            ]
        }
    },
    methods: {
        getImgPath(name) {
            return new URL(`../assets/img/${name.img}`, import.meta.url).href;
        }
        
}
} 
</script>

<template>
    <section class="container-footer">
        <div class="footer-top">
            <section class="link">
                <ul class="main-list">
                    <li v-for="(elements, index) in links" class="main-li">
                        <h3>{{ index }}</h3>
                        <ul>
                            <li v-for="item in elements"><a href="">{{ item.name }}</a></li>
                        </ul>
                    </li>

                </ul>
            </section>
        </div>
        <div class="footer-bot">
            <div class="bot-list">
                <a class="sign" href="">SIGN-UP</a>
                <ul class="cta">
                    <li><a href="">FOLLOW US</a></li>
                    <li v-for="icon in icons"><a :href="icon.url"><img :src="getImgPath(icon)" alt=""></a></li>
                </ul>
            </div>
        </div>
    </section>
</template>


<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.container-footer {
    height: calc(100vh - 370px);
    background-color: $footercolor;


    .footer-top {
        
        width: 100%;
        height: 450px;
        background-image: url(../assets/img/dc-logo-bg.png), url(../assets/img/footer-bg.jpg);
        background-position: center right, center center;
        background-repeat: no-repeat, repeat;
        background-size: 1, cover;

        .link {
            @include ms_container(100%, 0 auto);

            .main-list {
                padding-top: 50px;
                width: 50%;
                font-size: 1.3rem;
                flex-wrap: wrap;
                @include flex(row, flex-start, stretch);

                .main-li {
                    width: calc(100% / 3);
                    @include flex(column, flex-start, stretch);

                    h3 {
                        color: white;
                        margin-bottom: 20px;
                    }

                    &>ul>li {
                        font-size: .9rem;
                        color: rgb(133, 133, 133);
                        padding: 2px 0;

                    }
                }
            }
        }
    }

    .footer-bot {
        background-color: $footercolor;
        width: 100%;
        height: calc(100% - 450px);
        color: white;

        .bot-list {
            @include ms_container(100%, 0 auto);
            @include flex(row, space-between, center);

            .sign {
                padding: 10px;
                border: 3px solid $mainblu;
            }

            .cta {
                @include flex(row, center, center);
                color: $mainblu;
                gap: 8px;
                & li:nth-child(1){
                    width: 100px;
                    font-weight: bold;
                }
               

                li {
                    width: 50px;
                }

            }
        }

    }
}
</style>