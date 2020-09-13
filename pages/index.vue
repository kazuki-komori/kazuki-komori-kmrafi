<template>
  <div class="c-container p-Home">
    <div v-for="article in articles">
      <router-link :to="article.path">
        <Card>
          <div class="row">
            <section class="col-md-4">
              <img src="https://placehold.jp/150x150.png" alt="" class="p-Home__img">
            </section>
            <section class="col-md-8">
              <p class="p-Home__title">{{article.title}}</p>
              <p class="p-Home__description">{{article.description}}</p>
            </section>
          </div>
        </Card>
      </router-link>
    </div>
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

  &__img {
    height: 200px;
    object-fit: cover;
    border-radius: 10%;
  }

  &__title {
    color: #2f2f2f;
    font-weight: bold;
    font-size: 30px;
    text-decoration: none;
  }

  &__description {
    color: #2f2f2f;
    font-size: 23px;
    text-decoration: none;
  }

  a:hover {
    text-decoration: none;
  }
}
</style>
