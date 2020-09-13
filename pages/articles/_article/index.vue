<template>
  <div class="c-container p-article">
    <nuxt-content :document="article" />
  </div>
</template>

<script>
  export default {
    components: {},
    async asyncData({ $content, params }) {
      const article = await $content(`articles/${params.article}`).fetch();

      return {
        article
      };
    }
  };
</script>
<style lang="scss" scoped>
@import "@/assets/scss/mixins.scss";
.p-article {
  background-color: white;
  padding: 0 50px;
}
</style>
