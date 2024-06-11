<script>
export default {
    data() {
        return{

        }
    }
}
</script>

<template>
    <main>
        <section id="jumbotron">
            <img src="../img/jumbotron.jpg" alt="">
        </section>
        <section class="container">
            <p>
            --> Content goes here <--
            </p>
        </section>
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/mixins' as *;
    @use '../styles/partials/variables' as *;

    main {
        background-color: black;
        padding: 3rem 0;

        p{
            color: white;
            font-size: 1.5rem;
            font-weight: bold;
        }
    }

    section#jumbotron{
        height: 200px;
        background-size: cover;
        
    }
</style>