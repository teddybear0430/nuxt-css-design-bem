<template>
  <footer class="footer">
    <p class="footer__copyright">© {{ yearStr }} BEMの練習</p>
    <nav class="nav footer__nav">
      <ul class="nav__list">
        <li v-for="(link, i) in pageLinks" :key="i" class="nav__item">
          <a href="#">{{ link }}</a>
        </li>
      </ul>
    </nav>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'
import { pageLinks } from '../config/page-links'

export default defineComponent({
  setup() {
    const year = new Date().getFullYear()
    const yearStr = year.toString()

    return {
      pageLinks,
      yearStr,
    }
  },
})
</script>

<style lang="scss" scoped>
.footer {
  padding: 24px;
  color: #fff;
  background-color: #1a1a1a;
  display: flex;
  justify-content: space-between;
  align-items: center;

  &__nav {
    .nav__list {
      display: flex;
      justify-content: space-around;

      .nav__item {
        font-size: 12px;
        padding: 0 10px;
      }
    }
  }
}
</style>
