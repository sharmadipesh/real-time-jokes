<template>
    <div class="card-style home-card">
        <h2>Welcome to the best corny dad jokes app on the web.</h2>
    </div>
</template>

<script>
    export default {
        head: function(){
            return {
                title : 'Welcome to dad jokes',
                meta : [
                    {
                        hid : 'description',
                        name : 'description',
                        content : 'Best place for corny dad jokes..'
                    }
                ]
            }
        }
    }
</script>

<style>

    /* universal styling */
    *{
        margin:0;
        padding: 0;
    }

    /* custome fonts */
    @font-face {
        font-family: 'Righteous-Regular'; 
        src: url('~assets/fonts/Righteous-Regular.ttf');
    }

    .home-card{
        text-align: center;
        color: #fff;
        font-family: Righteous-Regular;
        font-size: 16px;
        background: linear-gradient(to right,#11998e,#38ef7d);
    }
</style>
