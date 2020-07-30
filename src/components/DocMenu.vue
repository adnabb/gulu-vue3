<template>
  <aside class="g-menu" v-if="menuVisible">
    <h2>组件列表</h2>
    <menu>
      <router-link to="/doc/switch">
        Switch 组件
      </router-link>
      <router-link to="/doc/button">
        Button 组件
      </router-link>
      <router-link to="/doc/dialog">
        Dialog 组件
      </router-link>
      <router-link to="/doc/tabs">
        Tabs 组件
      </router-link>
    </menu>
  </aside>
</template>

<script lang="ts">
import {inject} from 'vue';

export default {
  setup() {
    const menuVisible = inject('menuVisible');
    return {menuVisible}
  }
}
</script>

<style lang="scss" scoped>
.g-menu {
  position: fixed;
  background: #fff;
  border: 1px solid;
}

menu {
  display: flex;
  flex-direction: column;
}
</style>