<script>
export default {
    data() {
        return{
            footerLinks: [
            
            ]
        }
    }
}
</script>

<template>
    <footer>
        <section class="container">
            <section>
                <ul>

                </ul>
                <div id="bg-logo">
                </div>
            </section>
        </section>
        <section id="socials">    
            <section class="container">
                <button>sign-up now!</button>
                <div id="follow">
                    <p>Follow Us</p>
                    <img src="../img/footer-facebook.png" alt="">
                    <img src="../img/footer-twitter.png" alt="">
                    <img src="../img/footer-youtube.png" alt="">
                    <img src="../img/footer-pinterest.png" alt="">
                    <img src="../img/footer-periscope.png" alt="">
                </div>
            </section>
        </section>
    </footer>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixins' as *;
    @use '../styles/partials/variables' as *;

    footer{
        background-image: url(../img/footer-bg.jpg);
        height: 500px;

        section.container{
            @include flex-between();
        }
    }

    div#bg-logo{
        height: 450px;
        width: 450px;
        background-image: url(../img/dc-logo-bg.png);
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
    }

    section#socials{
        background-color: $bg-color-socials;
        padding: 1rem 0;
        @include uppercase-text();
    }

    button{
        padding: 1rem;
        border: 2px solid #0683F9;
        color: white;
        background-color: transparent;
        @include uppercase-text();
    }

    div#follow{
        @include flex-between();

            p,
            img{
                margin-right: 1rem;
            }

            p{
                color: white;
            }
    }

</style>