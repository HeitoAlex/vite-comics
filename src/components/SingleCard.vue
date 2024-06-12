<script>


export default {
    data() {
        return{
            
        }
    },

    props: {
        SingleComic: {
            type: Object,
            required: true
        }
    }
}
</script>

<template>
    
        <article>
            <img :src="SingleComic.thumb" :alt="SingleComic.series">
            <h4>
                {{ SingleComic.series }}
            </h4>
        </article>
    
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixins' as *;
    @use '../styles/partials/variables' as *;

    article{
        width: calc((100% / 6) - .5rem);
        padding: .5rem 3rem;
        margin-bottom: .5rem;
        margin-right: .5rem;

            img{
                width: 175px;
                height: 230px;
                margin-bottom: 1rem;
            }

            h4{
                @include uppercase-text();
                color: white;
                
            }
    }
</style>