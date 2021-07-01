<template>
  <div>
    <Tutorial/>
    <FirstView />
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api';
import FirstView from '../components/FirstView.vue';

export default defineComponent({
  components: {
    FirstView,
  },
});
</script>
