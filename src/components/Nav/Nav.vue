<template>
  <div class="nav">
    <router-link to="/goods" class="nav-item">
      点菜
      <i class="line"></i>
    </router-link>
    <router-link to="/ratings" class="nav-item">
      评价
      <i class="line"></i>
    </router-link>
    <router-link to="/seller" class="nav-item">
      商家
      <i class="line"></i>
    </router-link>
  </div>
</template>

<script>
  export default {
    name: "Nav"
  }
</script>

<style scoped>
  .nav {
    display: flex;
    width: 100%;
    height: 40px;
    line-height: 40px;
    border-bottom: 1px solid #e4e4e4;
  }

  .nav .nav-item {
    flex: 1;
    text-align: center;
    font-size: 13px;
    text-decoration: none;
    color: #666666;
    position: relative;
  }
  .nav .active {
    color: #FFBB22;
  }
  .nav .active .line {
    width: 20px;
    height: 2px;
    display: inline-block;
    position: absolute;
    background: #FFBB22;
    left: 50%;
    bottom: 0;
    margin-left: -10px;
  }

</style>
