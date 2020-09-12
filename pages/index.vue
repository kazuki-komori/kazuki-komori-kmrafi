<template>
  <div class="c-container p-Home">
    <Card>
      <div v-for="article in articles">
        <nuxt-link :to="article.path">{{article.title}}</nuxt-link>
      </div>
    </Card>
  </div>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const articles = await $content("articles")
    .limit(5)
    .fetch();
    return {
      articles
    }
  }
}
</script>

<style lang="scss" scoped>
@import "@/assets/scss/mixins.scss";
.p-Home {
  background-color: white;
  padding: 50px 0;
  height: 100vh;
}
</style>
