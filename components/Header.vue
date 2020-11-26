<template>
    <div class="header card-style">
        <div class="header-text">
            Welcome To Dad Jokesss!!!
        </div>
        <div class="header-link-container">
            <nuxt-link to="/">Home</nuxt-link>
            <nuxt-link to="/jokes">Jokes</nuxt-link>
            <nuxt-link to="/about">About</nuxt-link>
        </div>
    </div>
</template>

<script>
    export default {
        name:"Header"
    }
</script>

<style scoped>
    .header{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        margin-bottom: 25px;

        position: sticky;
        top: 0px;
    }
    .header-text{
        font-family: Righteous-Regular;
        font-weight: 900;
        font-size: 30px;
        text-shadow: 3px 3px 3px rgba(0,0,0,0.3);
        margin-bottom:8px;
        color: #363636;
    }

    .header-link-container a{
        color: #212121;
        font-size: 20px;
        margin: 0 8px;
        /* font-weight: 600; */
        font-style: italic;
        font-family: Righteous-Regular;
    }
    .header-link-container .nuxt-link-exact-active{
        color: #EB3349;
    }
</style>