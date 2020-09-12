<template>
  <div class="container">

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
