<template>
  <tab-bar>
      <tab-bar-item path="/home">
        <span slot="item-icon" class="iconfont icon-shouye"></span>
        <span slot="item-icon-active" class="iconfont icon-shouye_tianchong"></span>
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item path="/category">
        <span slot="item-icon" class="iconfont icon-fenlei"></span>
        <span slot="item-icon-active" class="iconfont icon-fenlei_tianchong"></span>
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item path="/cart">
        <span slot="item-icon" class="iconfont icon-gouwuche"></span>
        <span slot="item-icon-active" class="iconfont icon-gouwuche_tianchong"></span>
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item path="/profile">
        <span slot="item-icon" class="iconfont icon-wode"></span>
        <span slot="item-icon-active" class="iconfont icon-wode_tianchong"></span>
        <div slot="item-text">我的</div>
      </tab-bar-item>
  </tab-bar>
</template>

<script>
import TabBar from 'components/common/tabbar/TabBar'
import TabBarItem from 'components/common/tabbar/TabBarItem'
export default {
  name: "MainTabBar",
  components: {
    TabBar,
    TabBarItem
  }
};
</script>

<style>
</style>