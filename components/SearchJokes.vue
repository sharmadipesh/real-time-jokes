<template>
    <div class="card-style">
        <form @submit.prevent="searchHandler" class="form-style">
            <input type="text" v-model="text" placeholder="search text..." required class="search-input">
            <div>
                <input type="submit" value="search.." class="search-button">
            </div>
        </form>
    </div>
</template>

<script>
    export default {
        name : "SearchJokes",
        data :  function(){
            return {
                text:""
            }
        } ,
        methods:{
            searchHandler : function(){
                this.$emit('search-text',this.text);
                this.text="";
            }
        }
    }
</script>

<style scoped>
    .form-style{
        display: grid;
        grid-template-columns: 80% 20%;
    }
    .search-input{
        padding: 8px 10px;
        border-radius: 4px;
        border-color: #EB3349!important;
        transition: 0.2s;
        letter-spacing: 1.5px;
        font-family: Righteous-Regular;
    }
    .search-input:hover,.search-input:focus,.search-input:active{
        box-shadow: 0 2px 2px 2px rgba(235,51,73,0.5);
        transition: 0.2s;
    }
    .search-button{
        padding: 10px 15px;
        border: 0;
        border-radius: 4px;
        font-family: Righteous-Regular;
        background-color: #EB3349;
        color: #fff;
        cursor: pointer;
        transition: 0.2s;
        letter-spacing: 1px;
        margin-left: 20px;
    }
    .search-button:hover{
        box-shadow: 0 2px 2px 2px rgba(235,51,73,0.5);
        transition: 0.2s;
        letter-spacing: 2px;
    }
</style>
