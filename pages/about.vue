<template>
    <div class="card-style about-card">
        <h1>About Dad Jokes ://</h1>
        <p>This is an app that displays corny dad jokes....</p>
    </div>    
</template>

<script>
    export default {
        head: function(){
            return {
                title : 'About Us',
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

<style scoped>
    .about-card{
        color: #fff;
        font-family: Righteous-Regular;
        background: linear-gradient(to right,#ee0979,#ff6a00);
        text-align: center;
    }
</style>