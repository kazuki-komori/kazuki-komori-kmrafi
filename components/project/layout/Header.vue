<template>
  <section class="p-header">
    <div class="p-header__section c-container d-flex">
      <section class="d-flex align-items-center">
        <span class="p-header__icon material-icons d-block">
          accessibility_new
        </span>
        <span class="p-header__text d-block ml-2">
          Life
        </span>
      </section>
      <!--
      <section class="d-flex align-items-center ml-5">
        <span class="p-header__icon material-icons d-block">
          phonelink
        </span>
        <span class="p-header__text d-block ml-2">
          Device
        </span>
      </section>
      -->
    </div>
  </section>
</template>
<script></script>
<style lang="scss" scoped>
@import "@/assets/scss/mixins.scss";
.p-header {
  background-color: #2f2f2f;

  &__section {
    width: 100%;
    height: 80px;
    color: white;
  }

  &__icon {
    font-size: 40px;
    vertical-align: middle;
  }

  &__text {
    font-size: 40px;
    vertical-align: middle;
  }
}
</style>
