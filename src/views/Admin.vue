<template>
  <div class="admin">
    <div id="nav">
      <router-link to="/">前台首頁</router-link> |
      <router-link to="/admin/products">產品管理</router-link> |
      <router-link to="/admin/coupons">優惠券列表</router-link> |
      <router-link to="/admin/orders">訂單列表</router-link> |
      <router-link to="/admin/files">圖片列表</router-link> |
      <a href="#" @click.prevent="logout">登出</a>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  methods: {
    logout() {
      document.cookie = 'AUTH_TOKEN=; expires=; path=/';
      this.$router.push('/login');
    },
  },
};
</script>
