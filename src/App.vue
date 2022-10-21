<template>
  <NavBar :title="titleTonav"/>
  <h2 class="heading"><span class="made">Made</span> with <span class="span-head">Vue.Js</span> with ❤ by <span class="span-head">Danish !</span></h2>
  <News/>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import News from "./components/News.vue";
export default {
  components: { NavBar, News },
  data(){
    return{
    
      titleTonav:'NewsWallah',

    };
  },
};
</script>

<style>
.heading{
  text-align: center;
  margin-top:8px;
  margin-bottom: 8px;
}
.span-head{
  color: #96C93C;
}
.made{
  color: #E81224;
}

</style>