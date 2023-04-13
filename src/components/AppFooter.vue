<script>
export default {
    name: "AppFooter",
    data() {
    }
} 
</script>

<template>
    <section class="container-footer">
        <div class="footer-top">
            <section class="link">
                <ul class="main-list">
                    <li class="main-li">
                        <h3>DC COMICS</h3>
                        <ul>
                            <li><a href="">Characters</a></li>
                            <li><a href="">Comics</a></li>
                            <li><a href="">Movies</a></li>
                            <li><a href="">TV</a></li>
                            <li><a href="">Games</a></li>
                            <li><a href="">Videos</a></li>
                            <li><a href="">News</a></li>
                        </ul>
                    </li>

                    <li class="main-li">
                        <h3>DC</h3>
                        <ul>
                            <li><a href="">Terms </a></li>
                            <li><a href="">Policy </a></li>
                            <li><a href="">Choise </a></li>
                            <li><a href="">Adv </a></li>
                            <li><a href="">Jobs </a></li>
                            <li><a href="">Subscription </a></li>
                            <li><a href="">Talent Workshop </a></li>
                            <li><a href="">Ratings </a></li>
                            <li><a href="">Shop </a></li>
                            <li><a href="">Contact US </a></li>
                        </ul>
                    </li>

                    <li class="main-li">
                        <h3>SITES</h3>
                        <ul>
                            <li><a href="">Dc</a></li>
                            <li><a href="">MAD Magazine</a></li>
                            <li><a href="">DC kids</a></li>
                            <li><a href="">DC Universe</a></li>
                            <li><a href="">DC Powervisa</a></li>
                        </ul>
                    </li>
                    <li  class="main-li shop">
                        <h3>SHOP</h3>
                        <ul>
                            <li><a href="">DC shop</a></li>
                            <li><a href="">Collec</a></li>
                        </ul>
                    </li>
                </ul>
            </section>
        </div>
        <div class="footer-bot">

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
                @include ms_container(100%,0 auto);
            .main-list {
                padding-top: 50px;
                width: 50%;
                font-size: 1.3rem;
                flex-wrap: wrap;
                @include flex(row, flex-start, stretch);

                .main-li {
                    width: calc(100% / 3);
                    @include flex(column, flex-start, stretch);
                    h3{
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
    }
}
</style>