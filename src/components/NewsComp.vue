<template>
  <div class="card newscomp" style="width: 18rem">
    <img :src="article.urlToImage" class="card-img-top" alt= />
    <div class="card-body">
      <h5 class="card-title">{{ article.title }}</h5>
      <p class="card-text">
        {{article.content}}
      </p>
      <a href="#" class="btn btn-primary">Read More</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "NewsComp",
  props: ["article"],
};
</script>

<style>
.newscomp {
  margin: 10px;
}
</style>