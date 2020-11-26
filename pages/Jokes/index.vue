<template>
    <div>
        <SearchJokes v-on:search-text="searchHandler"/>
        <div>
            <Joke 
                v-for="joke in jokes"  
                v-bind:key="joke.id"
                v-bind:joke="joke.joke"
                v-bind:id="joke.id"
            />
        </div>
    </div>    
</template>

<script>

    import axios from 'axios';
    import Joke from '../../components/Joke';
    import SearchJokes from '../../components/SearchJokes';

    export default {
        data: function(){
            return {
                jokes : []
            }
        },
        components:{
            Joke,
            SearchJokes
        },
        created: async function(){
            const config = {
                headers : {
                    'Accept' : 'application/json'
                }
            }
            try{
                const res = await axios.get('https://icanhazdadjoke.com/search',config);
                this.jokes = [...res.data.results] ;
            }catch(err){
                console.log("===== Error ====",err)
            }
        },
        head: function(){
            return {
                title : 'Dad Jokes',
                meta : [
                    {
                        hid : 'description',
                        name : 'description',
                        content : 'Best place for corny dad jokes..'
                    }
                ]
            }
        },
        methods:{
            searchHandler: async function(search_text){
                // console.log("=========== SEARCH ++÷");
                const config = {
                    headers : {
                        'Accept' : 'application/json'
                    }
                }
                try{
                    const res = await axios.get(`https://icanhazdadjoke.com/search?term=${search_text}`,config);
                    this.jokes = [...res.data.results] ;
                }catch(err){
                    console.log("===== Error ====",err)
                }
            }
        }
    }
</script>

<style scoped>

</style>