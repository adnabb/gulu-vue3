<template>
  <g-header></g-header>
  <doc-menu></doc-menu>
  <main>
    <router-view></router-view>
  </main>
</template>

<script lang="ts">
import GHeader from '../components/Header.vue';
import DocMenu from '../components/DocMenu.vue';

  export default {
    name: "doc",
    components: {
      GHeader,
      DocMenu
    }
  }
</script>

<style lang="scss" scoped>

</style>