<template>
  <router-view />
</template>

<script lang="ts">
import { ref, provide } from 'vue';

export default {
  name: 'App',
  setup() {
    const width = document.documentElement.clientWidth;
    console.log(width, width > 500)
    const menuVisisble = ref(width > 500);
    provide('menuVisible', menuVisisble);
  }
}
</script>
