<script>
import json from "../vue-dc-comics-2/dc-comics.json"

export default {
    data() {
        return{
            myJason: json
        }
    }
}
</script>

<template>
    <main>
        <section id="jumbotron">
            
        </section>
        <section class="container">
            <SingleCard v-for="(, price) in myJason[item]"/>
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
</style>