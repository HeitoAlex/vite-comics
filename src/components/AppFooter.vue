<script>
export default {
    data() {
        return{
            dcComics: [
                {
                    id: 1,
                    title: 'Characters',
                    url: '#'
                },
                {
                    id: 2,
                    title: 'Comics',
                    url: '#'
                },
                {
                    id: 3,
                    title: 'Movies',
                    url: '#'
                },
                {
                    id: 4,
                    title: 'TV',
                    url: '#'
                },
                {
                    id: 5,
                    title: 'Games',
                    url: '#'
                },
                {
                    id: 6,
                    title: 'Videos',
                    url: '#'
                },
                {
                    id: 7,
                    title: 'News',
                    url: '#'
                }
            ],
            shop:[
                {
                    id: 1,
                    title: 'Shop DC',
                    url: '#'
                },
                {
                    id: 2,
                    title: 'Shop DC Collectibles',
                    url: '#'
                }
            ],
            dc: [
                {
                    id: 1,
                    title: 'Term Of Use',
                    url: '#'
                },
                {
                    id: 2,
                    title: 'Privacy policy (New)',
                    url: '#'
                },
                {
                    id: 3,
                    title: 'Ad Choices',
                    url: '#'
                },
                {
                    id: 4,
                    title: 'Advertising',
                    url: '#'
                },
                {
                    id: 5,
                    title: 'Job',
                    url: '#'
                },
                {
                    id: 6,
                    title: 'Subscription',
                    url: '#'
                },
                {
                    id: 7,
                    title: 'Talent Workshop',
                    url: '#'
                },
                {
                    id: 8,
                    title: 'CPSC Certificates',
                    url: '#'
                },
                {
                    id: 9,
                    title: 'Ratings',
                    url: '#'
                },
                {
                    id: 10,
                    title: 'Shop Help',
                    url: '#'
                },
                {
                    id: 11,
                    title: 'Contact Us',
                    url: '#'
                },
            ],
            sites: [
                {
                    id: 1,
                    title: 'DC',
                    url: '#'
                },
                {
                    id: 2,
                    title: 'MAD Magazine',
                    url: '#'
                },
                {
                    id: 3,
                    title: 'DC Kids',
                    url: '#'
                },
                {
                    id: 4,
                    title: 'DC Universe',
                    url: '#'
                },
                {
                    id: 5,
                    title: 'DC Power Visa',
                    url: '#'
                }
            ]
        }
    }
}
</script>

<template>
    <footer>
        <section class="container">
            <div id="footer-links">
                <div>
                    <h3>DC COMICS</h3>
                    <ul>
                        <li v-for="link in dcComics" :key="link.id">
                            <a href="link.url">
                                {{ link.title }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3>SHOP</h3>
                    <ul>
                        <li v-for="link in shop" :key="link.id">
                            <a href="link.url">
                                {{ link.title }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3>DC</h3>
                    <ul>
                        <li v-for="link in dc" :key="link.id">
                            <a href="link.url">
                                {{ link.title }}
                            </a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3>SITES</h3>
                    <ul>
                        <li v-for="link in sites" :key="link.id">
                            <a href="link.url">
                                {{ link.title }}
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
            <div id="bg-logo">
            </div>
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
        position: relative;

        section.container{
            @include flex-between();
        }
    }

    div#footer-links{
        @include flex-column();
        height: 350px;
        margin-top: 5rem;
            
            div{
                margin-bottom: 1rem;
                margin-right: 1.5rem;
            }

            h3{
                margin-bottom: 1rem;
                color: white;
                font-weight: bold;
            }

            li{
                margin-bottom: .2rem;
                font-size: .8rem;
            }

            li a{
                color: gray;
            }
    }

    div#bg-logo{
        height: 500px;
        width: 500px;
        background-image: url(../img/dc-logo-bg.png);
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
    }

    section#socials{
        background-color: $bg-color-socials;
        padding: 1.5rem 0;
        @include uppercase-text();
        position: absolute;
        right: 0;
        left: 0;
        bottom: 0;
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