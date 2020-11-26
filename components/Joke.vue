<template>
    <!-- for dynamic we used colon :to -->
    <nuxt-link :to="'jokes/' + id">
        <div class="card-style joke-card-style">
            <div>{{ joke }}</div>
        </div>
    </nuxt-link>
</template>

<script>
    export default {
        name:'Joke',
        props:{
            joke : String,
            id : String,
        },
    }
</script>

<style scoped>
    .joke-card-style{
        margin: 20px 0;
        font-family: Righteous-Regular;
        color: #ffffff;
        background: linear-gradient(to right,#FF512F,#DD2476);
    }
</style>
