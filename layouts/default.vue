<template>
    <div class="layout-container">
        <div></div>
        <div>
            <Header />
            <div>
                <Nuxt />
            </div>
        </div>
        <div></div>
    </div>
</template>

<script>

    import Header from "../components/Header";

    export default {
        components:{
            Header
        }
    }

</script>

<style>
    .layout-container{
        display: grid;
        grid-template-columns:33.33% 33.33% 33.33%;
        margin: 30px 40px;
    }

    .card-style{
        background-color: #fff;
        border-radius: 10px;
        border: 2px solid transparent;
        transition: 0.3s;
        box-shadow: 0 3px 6px rgba(0,0,0,0.16), 0 3px 6px rgba(0,0,0,0.23);
        padding: 20px;
    }
</style>
