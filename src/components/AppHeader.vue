<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: true
                },
                {
                    text: "MOVIES",
                    url: "#",
                    current: false
                },
                {
                    text: "TV",
                    url: "#",
                    current: false
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false
                }
            ]
        }
    }
} 
</script>

<template>
    <div class="container-header">
        <header>
            <div class="logo"><a href=""><img src="../assets/img/dc-logo.png" alt=""></a>
            </div>
            <nav>
                <ul>
                    <li v-for="link in links"><a href="">{{ link.text }}</a></li>
                </ul>
            </nav>
        </header>
    </div>
</template>


<style scoped lang="scss">
@use "../style/partials/mixins" as *;
@use "../style/partials/variables" as *;


.container-header {
    background-color: white;

    header {
        @include ms_container;

        @include flex(row, space-between, center);

        ul {
            list-style-type: none;
            @include flex(row, center, center);
            gap: 10px;

            li {
                font-size: 12px;
                line-height: 120px;
                &:hover{
                        border-bottom: 5px solid $features;
                    }
                
                a {
                    text-decoration: none;
                    color: $textcolor;
                    &:hover{
                        color: $features;
                    }
                }
            }
        }
    }
}
</style>
