<script>
export default {
    name: "AppFeatures",
    data() {
        return {
            shopLinks: [
                {
                    img: "buy-comics-digital-comics.png",
                    title: "digital comics",
                    url: "#",
                },
                {
                    img: "buy-comics-merchandise.png",
                    title: "dc merchandise",
                    url: "#",
                },
                {
                    img: "buy-comics-subscriptions.png",
                    title: "subscription",
                    url: "#",
                },
                {
                    img: "buy-comics-shop-locator.png",
                    title: "comic shop locator",
                    url: "#",
                },
                {
                    img: "buy-dc-power-visa.svg",
                    title: "dc power visa",
                    url: "#",
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
    <div class="features">
        <ul class="ancor-link">
            <li v-for="element in shopLinks">
                <a :href="element.url">
                    <img :src="getImgPath(element)" alt="">
                    <h3>{{ element.title }}</h3>
                </a>
            </li>
        </ul>
    </div>
</template>


<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;

.features {
    width: 100%;
    height: 150px;
    background-color: $mainblu;

    .ancor-link {
        @include flex(row, space-around, center);
        @include ms_container(100%, 0 auto);

        li {
            width: 50px;
            font-size: .4rem;
            color: white;

            &:nth-child(4) {
                width: 30px;
            }
                a {
                    @include flex(column, center, center);
                    gap: 10px;


                    h3 {
                        font-size: 1rem;
                        text-align: center;
                    }
                }
            }
        }
    }
</style>
