<template>
    <div id="main">
        <div class="header">
            <div class="header-container">
                <div class="logo"><img src="/img/madewithvue.svg" alt=""></div>
                <div class="nav">
                    <a href="#">Home</a>
                    <a href="#">About Us</a>
                    <a href="#">Contact Us</a>
                </div>
            </div>
        </div>
        <div id="carousel">
        <div class="attach">
            <div class="slider_case">
                <v-slider v-bind="options">
                    <a class="item" href="#"></a>
                    <a class="item" href="#"></a>
                    <a class="item" href="#"></a>
                    <a class="item" href="#"></a>
                    <a class="item" href="#"></a>
                    <a class="item" href="#"></a>
                    <a class="item" href="#"></a>
                    <a class="item" href="#"></a>
                    <a class="item" href="#"></a>
                </v-slider>
            </div>
        </div>
        </div>
    </div>
</template>

<script>
    import slider from './slider.vue'

    export default {
        name: 'main',

        data () {
            return {
                options: {
                    items: 3,
                    margin: 40,
                    nav: true,
                    dots: false,
                    loop: true,
                    offset: 1,
                    prevNav: '<',
                    nextNav: '>',
                    sibling: true,
                    responsive : {
                        0: {
                            items: 1
                        },
                        768: {
                            items: 2
                        },
                        999: {
                            items: 3
                        }
                    }
                }
            }
        },

        components: {
            'v-slider': slider,
        }
    }
</script>

<style scoped>
    @import url('https://fonts.googleapis.com/css?family=Ubuntu');

    * {
        margin: 0;
        padding: 0;
        border:0;
        max-height: 99999999px;
        box-sizing: border-box;
    }

    body {min-width: 320px;
        margin: 0}

    .header-container {
        width: 70%;
        margin: 0 auto;
        display: flex;
        flex-direction: row;
        align-items: center;
        height: 100%;
        justify-content: center;
    }

    .header {
        width: 100%;
        position: fixed;
        height: 50px;
        background-color: #35485d;
        z-index: 101;
        left: 0;
        border-radius: 5px;
        font-family: 'Ubuntu', sans-serif;
    }


    .nav {

    }

    .nav a {
        margin-right: 30px;
        display: inline-block;
        color: #41b883;
        text-decoration: none;
        transition: 0.5s ease all;
        font-size: 20px;
        font-weight: bold
    }
    .logo img {width: 350px;}
    .logo {position: absolute; left: 10px}
    .nav a:last-child {
        margin-right: 0
    }

    .nav a:before {
        content: "~";
        margin-right: 10px;
    }

    .nav a:hover {
        color: #3b8070;
    }


    #main {
        font-family: 'Ubuntu', sans-serif;
        font-size: 14px;
    }

    .attach {
        width: 100%;
        max-width: 1000px;
        min-width: 480px;
        padding: 50px 15px;
        margin: 0 auto;
        position: relative;
    }
    #carousel {
        padding-top: 250px
    }
    .slider_case {
        margin-bottom: 40px;
    }

    .item {
        background: url(/img/vue.png) no-repeat center;
        text-align: center;
        padding: 100px 0;
        color: #fff;
        font-size: 20px;
        font-weight: 300;
        text-decoration: none;
        display: inline-block;
        height: 220px;
        background-size: cover;
    }

    @media (max-width: 1199px) {
        .logo {display: none}
    }

    @media (max-width: 767px) {
        html {min-width: 320px}
        .header {height: 150px}

        .nav {
            margin: auto;
        }

        .nav a {
            font-size: 22px;
            display: block;

        }
    }






</style>