<template>
  <div class="home">
    <left-menu></left-menu>
    <div :class="{ 'main-app': true, 'menu-unfold': $store.state.collapsed }">
     <silderNav></silderNav>
     <router-view></router-view>
    </div>
  </div>
</template>

<script>
import LeftMenu from './components/menu.vue';
import silderNav from './components/sliderNav.vue';

export default {
  components: {
    LeftMenu,
    silderNav,
  },
};
</script>

<style lang="less">
@import url("~@/assets/css/home.less");
</style>
