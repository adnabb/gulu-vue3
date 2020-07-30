<template>
  <div class="g-header">
    <i class="menu-toggle" @click="toggleMenu">toogle</i>
    <router-link to="/">
      <img width="30" src="../assets/logo.png" alt="logo">
    </router-link>
    <nav>导航栏</nav>
  </div>
</template>

<script lang="ts">
  import {inject, Ref} from 'vue';

  export default {
    name: "g-header",
    setup() {
      const menuVisible = inject<Ref<Boolean>>('menuVisible');
      const toggleMenu = () => {
        menuVisible.value = !menuVisible.value;
      };
      return { toggleMenu };
    }
  }
</script>

<style lang="scss" scoped>
  .g-header {
    display: flex;
    justify-content: space-between;
    .menu-toggle {
      visibility: hidden;
      cursor: pointer;
    }
    img {

    }
    nav {

    }
    @media (max-width: 500px) {
      .menu-toggle {
        visibility: visible;
        border: 1px solid;
      }
      nav {
        visibility: hidden;
      }
    }
  }
</style>