<template>
  <header class="header">
    <h1 class="header__logo">ヘッダー</h1>
    <nav class="nav header__nav">
      <ul class="nav__list">
        <li class="nav__item"><a href="#">ホーム</a></li>
        <li class="nav__item"><a href="#">特徴</a></li>
        <li class="nav__item"><a href="#">サービス</a></li>
        <li class="nav__item"><a href="#">ニュース</a></li>
        <li class="nav__item"><a href="#">ブログ</a></li>
      </ul>
    </nav>
  </header>
</template>

<script lang="ts">
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
