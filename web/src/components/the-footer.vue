<template>
  <a-layout-footer style="text-align: center">
    Ebook Management System<span v-show="user.id">，Welcome：{{user.name}}</span>
  </a-layout-footer>
</template>

<script lang="ts">
import { defineComponent, computed } from 'vue';
import store from "@/store";

export default defineComponent({
  name: 'the-footer',
  setup() {
    const user = computed(() => store.state.user);

    return {
      user
    }
  }
});
</script>
