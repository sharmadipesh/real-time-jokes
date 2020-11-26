<template>
    <div>
        <nuxt-link to="/jokes">Back to Jokes</nuxt-link>
        <div class="card-style single-joke">
            <div class="">
                {{joke.joke}}
            </div>
            <hr class="hr-line">
            <div>
                {{this.$route.params.id}}
            </div>
        </div>
    </div>
</template>

<script>

    import axios from 'axios';

    export default {
        data: function(){
            return {
                joke:{}
            }
        },
        created : async function(){
            const config = {
                headers : {
                    'Accept' : 'application/json'
                }
            }
            try{
                const res = await axios.get(`https://icanhazdadjoke.com/j/${this.$route.params.id}`,config);
                this.joke = {
                    ...res.data
                }
            }catch(err){
                console.log("======== ",err)
            }
        }
    }
</script>

<style scoped>
    .single-joke{
        background: linear-gradient(to right,#76b852,#8DC26F);
        color: #fff;
        font-family: Righteous-Regular;
        margin-top: 15px;
    }
    .hr-line{
        margin: 10px 0;
    }

    .nuxt-link-active{
        font-family: Righteous-Regular;
        color: #212121;
        transition: 0.3s;
    }
    .nuxt-link-active:hover{
        transition: 0.3s;
        color: #EB3349;
    }
</style>