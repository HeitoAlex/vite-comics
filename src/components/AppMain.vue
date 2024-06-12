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
            
        </section>
        <section>
            <div class="container card">
                <SingleCard v-for="(item, index) in myJason" :key="index" :SingleComic="item"/>
            </div>
            <button>
                Load more
            </button>
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
        
    }

    section{
        background-color: black;
        padding: 1rem;
    }

    .card{
        @include flex-center()
    }
</style>