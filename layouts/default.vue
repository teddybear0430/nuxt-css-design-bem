<template>
  <div id="app">
    <Header />
    <Nuxt />
    <Footer />
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api';
import Header from '../components/Header.vue';
import Footer from '../components/Footer.vue';

export default defineComponent({
  components: {
    Header,
    Footer,
  },
});
</script>
