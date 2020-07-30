<template>
  <g-header></g-header>
  <main class="banner">
    <img src="../assets/logo.png" alt="logo">
    <h1>咕噜UI</h1>
    <h2>一个厉害的 UI 框架</h2>
    <p class="actions">
      <a href="">GitHub</a>
      <router-link to="/doc">开始</router-link>
    </p>
  </main>
</template>

<script lang="ts">
import GHeader from '../components/Header.vue';

  export default {
    name: "home",
    components: {
      GHeader
    }
  }
</script>

<style lang="scss" scoped>
.banner {
  text-align: center;
}
.actions {
  a {
    margin-right: 20px;
  }
}
</style>