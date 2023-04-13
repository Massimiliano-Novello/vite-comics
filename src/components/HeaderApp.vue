<script>
export default {
    name: "HeaderApp",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    current: false
                },
                {
                    text: "COMICS",
                    current: true
                },
                {
                    text: "MOVIES",
                    current: false
                },
                {
                    text: "TV",
                    current: false
                },
                {
                    text: "GAMES",
                    current: false
                },
                {
                    text: "COLLECTIBLES",
                    current: false
                },
                {
                    text: "VIDEOS",
                    current: false
                },
                {
                    text: "FANS",
                    current: false
                },
                {
                    text: "NEWS",
                    current: false
                },
                {
                    text: "SHOP",
                    current: false
                },
            ]
        }
    }
}
</script>


<template>
<header class="header">
    <a class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
    </a>
    <div class="header-rigth">
        <ul class="list">
            <li v-for="link in links" :class="{'active': link.current === true}">
                <a href="">
                    {{ link.text }}
                </a>
            </li>

        </ul>
    </div>
</header>

<section class="jumbotron">
    <div class="content">
        <h3>--> Content goes here &lt;-- </h3>

    </div>
</section>

</template>


<style lang="scss" scoped>

@use "../style/partials/mixins" as *;
@use "../style/partials/variabals" as *;
.header {
    width: 70%;
    height: 140px;
    margin: 0 auto;

    @include flex (row, space-between, center);

    img {
        width: 80px;
    }

    .list {
        @include flex (row, space-between, center);
    }

    li {
        list-style: none;
        margin: 0 .4rem;

        &.active {
            border-bottom: 2px solid blue;
        }
    }

    a {
        text-decoration: none;
        font-size: .8rem;
        font-weight: 500;
        color: $text-color;
    }


}

.jumbotron {
    height: 140px;
    background-color: $text-color;

    .content {
        width: 70%;
        height: 100%;
        margin: 0 auto;

        @include flex (row, start, center);

        h3 {
            font-size: 1.5rem;
            color: $color-title;
        }
    }
}
</style>