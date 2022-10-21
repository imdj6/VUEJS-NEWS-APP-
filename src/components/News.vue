<template>
    <div class="news">
        <NewsComp v-for="(news,index) in article" :key="index" :article='news'/>
    </div>
</template>

<script>
import NewsComp from './NewsComp.vue';
export default {
    components: { NewsComp },
    data(){
        return{
            article:[]
        }     
    },
    mounted (){
    const getarticles=async ()=> {
        const articals=await fetch('https://newsapi.org/v2/top-headlines?country=in&apiKey=a76ae486afb44b3fb35d722e0e4e1d41');
        const data=await articals.json();
        this.article=data.articles;
    }
    getarticles();
    }
};
</script>

<style>
.news{
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
    
}
</style>