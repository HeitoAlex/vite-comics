<script>
export default {
    data() {
        return{
            headerLinks: [
                {
                    id: 1,
                    title: 'characters',
                    active: false,
                    url: '#'
                },
                {
                    id: 2,
                    title: 'comics',
                    active: true,
                    url: '#'
                },
                {
                    id: 3,
                    title: 'movies',
                    active: false,
                    url: '#'
                },
                {
                    id: 4,
                    title: 'tv',
                    active: false,
                    url: '#'
                },
                {
                    id: 5,
                    title: 'games',
                    active: false,
                    url: '#'
                },
                {
                    id: 6,
                    title: 'collectibles',
                    active: false,
                    url: '#'
                },
                {
                    id: 7,
                    title: 'videos',
                    active: false,
                    url: '#'
                },
                {
                    id: 8,
                    title: 'fans',
                    active: false,
                    url: '#'
                },
                {
                    id: 9,
                    title: 'news',
                    active: false,
                    url: '#'
                },
                {
                    id: 10,
                    title: 'shop',
                    active: false,
                    url: '#'
                },
            ]
        }
    }
}
</script>

<template>
    <header class="container">
        <section>
            <img src="../img/dc-logo.png" alt="dc logo">
        </section>
        <section>
            <nav>
                <ul>
                    <li v-for="link in headerLinks" :key="link.id" :class="(link.active) ? 'active' : ''">
                        <a href="link.url">
                            {{ link.title }}
                        </a>
                    </li>
                </ul>
            </nav>
        </section>
    </header>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixins' as *;
    @use '../styles/partials/variables' as *;

    header{
        @include flex-between();
        padding: 1rem 0;
    }

    ul{
        @include flex-between();
            
            li{
            font-size: .8rem;
            font-weight: bold;
            text-transform: uppercase;
            margin-right: 1.3rem;

                a {
                    &active{
                        color: $color-active-link;
                    }
                }
            }
    } 




</style>
