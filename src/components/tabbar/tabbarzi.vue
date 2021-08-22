<template>
  <one>
<two path="/home" activeColor="red">
      <img slot="item-icon" src="../../assets/img/tabbar/home.svg" alt="">
      <img slot="item-icon-active" src="../../assets/img/tabbar/home_active.svg" alt="">
      <div slot="item-text">首页</div>
    </two>
    <two path="/category" activeColor="red">
      <img slot="item-icon" src="../../assets/img/tabbar/category.svg" alt="">
      <img slot="item-icon-active" src="../../assets/img/tabbar/category_active.svg" alt="">
      <div slot="item-text">分类</div>
    </two>
    <two path="/cart" activeColor="red">
      <img slot="item-icon" src="../../assets/img/tabbar/shopcart.svg" alt="">
      <img slot="item-icon-active" src="../../assets/img/tabbar/shopcart_active.svg" alt="">
      <div slot="item-text">购物车</div>
    </two>
    <two path="/profile" activeColor="deepPink">
      <img slot="item-icon" src="../../assets/img/tabbar/profile.svg" alt="">
      <img slot="item-icon-active" src="../../assets/img/tabbar/profile_active.svg" alt="">
      <div slot="item-text">我的</div>
    </two>
  </one>
</template>

<script>
import one from "./first.vue";
import two from "./second.vue";

export default {
  name: "tabbarzi",
  components: {
    one,
    two,
  },
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
