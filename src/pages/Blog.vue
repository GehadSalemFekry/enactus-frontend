<template>
    <div class="blog" dir="auto">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <h1 class="heading">{{ $t('blog.blog-title')}}</h1>
                    <hr />
                </div>
            </div>
            
            <Article v-for="(article, index) in this.$store.state.articles" :key="article.id" :article="article" :index="index">
            
            </Article>
        </div>
        
        
        
        
  </div>
</template>
<script>
import Article from "../components/Article";

export default {
  components: {
    Article,
  },

  created() {
    this.$store.dispatch("retrieveArticles");
  },
};
</script>
<style lang="">
</style>