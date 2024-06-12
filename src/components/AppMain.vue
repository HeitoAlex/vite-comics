<script>
import json from "../vue-dc-comics-2/dc-comics.json"
import SingleCard from "./SingleCard.vue";

export default {
    data() {
        return{
            myJason: json
        }
    },
    components: {
        SingleCard
    }
}
</script>

<template>
    <main>
        <section id="jumbotron">
            <div>
                Current series
            </div>
        </section>
        <section>
            <div class="container card">
                <SingleCard v-for="(item, index) in myJason" :key="index" :SingleComic="item"/>
            </div>
            <div id="load">
                <button>
                Load more
                </button>
            </div>
        </section>
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixins' as *;
    @use '../styles/partials/variables' as *;

    section#jumbotron{
        background-image: url(../img/jumbotron.jpg);
        height: 300px;
        background-size: cover;
        position: relative;

            div{
                position: absolute;
                @include uppercase-text();
                background-color: $color-active-link;
                color: white;
                padding: 1rem 2rem;
                bottom: -1.5rem;
                left: 12rem;
                font-weight: bolder;
            }
    }

    section{
        background-color: black;
        padding: 2rem;
    }

    .card{
        @include flex-center()
    }

    div#load{
        @include flex-center()
    }

    button{
    @include uppercase-text();
    background-color: $color-active-link;
    color: white;
    padding: 1rem 4rem;
    border: none;
    font-weight: bolder;
    }

    
</style>