<script>
export default {
    name: "FooterApp",
    data() {
        return {

        }
    }
}
</script>


<template>
    <footer class="footer">
        <div class="footer-content">
            <div class="btn">
                <a href="">
                    Sign up Now
                </a>
            </div>
            <div class="icons">
                <div class="icons-title">
                    <h3>FOLLOW US</h3>
                </div>
                <div class="icons-image">
                    <img src="../assets/img/footer-facebook.png" alt="">
                    <img src="../assets/img/footer-periscope.png" alt="">
                    <img src="../assets/img/footer-pinterest.png" alt="">
                </div>
            </div>
        </div>
    </footer>
</template>


<style lang="scss" scoped>
@use "../style/partials/mixins" as *;
@use "../style/partials/variabals" as *;

footer {
    background-color: $footer-color;
    height: 100px;


    .footer-content {
        width: 70%;
        height: 100%;
        margin: 0 auto;

        @include flex (row, space-between, center);

        a {
            text-decoration: none;
            color: $color-title;
            font-size: 1rem;
            border: 2px solid blue;
            padding: 10px;
        }

        .icons {
            @include flex (row, center, center);

            .icons-title {
                color: $main-color;
                margin: 0 .5rem;
            }
            img {
                width: 30px;
                margin: 0 .5rem;
            }
        }

    }
}


</style>