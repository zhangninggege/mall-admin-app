<template>
  <div class="main-header">
    <a-button
      type="primary"
      style="margin-bottom: 16px"
      @click="toggleCollapsed"
    >
      <a-icon :type="$store.state.collapsed ? 'menu-unfold' : 'menu-fold'" />
    </a-button>
    <div class="ant-breadcrumb">
      <a-breadcrumb>
        <a-breadcrumb-item>首页</a-breadcrumb-item>
        <a-breadcrumb-item><a href="">统计</a></a-breadcrumb-item>
      </a-breadcrumb>
    </div>
    <ul class="user-info">
      <li class="user-name">
        {{ $store.stute.user.username }}
        <a-icon type="down" />
      </li>
      <li>退出登录</li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {

    };
  },

  methods: {
    toggleCollapsed() {
      this.$store.dispatch('changeCollapsed');
    },

  },
};
</script>
