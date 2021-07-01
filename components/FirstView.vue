<template>
  <div>
    <h2>Test</h2>
    <div>{{ state.count }}</div>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive } from '@nuxtjs/composition-api';

export default defineComponent({
  setup() {
    const state = reactive({
      count: 0
    })

    return {
      state
    }
  },
});
</script>
