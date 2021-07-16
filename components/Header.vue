<template>
  <header class="header">
    <h1 class="header__logo">ヘッダー</h1>
    <nav class="nav header__nav">
      <ul class="nav__list">
        <li v-for="(link, i) in pageLinks" :key="i" class="nav__item">
          <a href="#">{{ link }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api';
import { pageLinks } from '../config/page-links';

export default defineComponent({
  setup() {
    return {
      pageLinks,
    }
  },
});
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 70px;
  width: 100%;
  padding: 0 24px;
  border-bottom: 1px solid #eee;
  background-color: #fff;
  position: sticky;
  left: 0;
  top: 0;
  z-index: 10;

  &__nav {
    .nav__list {
      display: flex;
      justify-content: space-around;
      width: 100%;
      min-width: 645px;

      .nav__item {
        font-size: 14px;
        font-weight: bold;
      }
    }
  }
}
</style>
