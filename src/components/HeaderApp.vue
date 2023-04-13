<script>
export default {
    name: "HeaderApp",
    data() {
        return {
            links: [
                {
                    text: "characters",
                    current: false
                },
                {
                    text: "comics",
                    current: true
                },
                {
                    text: "movies",
                    current: false
                },
                {
                    text: "tv",
                    current: false
                },
                {
                    text: "games",
                    current: false
                },
                {
                    text: "collectibles",
                    current: false
                },
                {
                    text: "videos",
                    current: false
                },
                {
                    text: "fans",
                    current: false
                },
                {
                    text: "news",
                    current: false
                },
                {
                    text: "shop",
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
        color: $text-color;
    }


}
</style>