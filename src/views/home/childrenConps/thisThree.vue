<template>
  <div class="thisThree">
    <div class="threetwo" v-for="item in recommend" :key="item">
      <a href="https://baidu.com">
        <img :src="item.image" alt="" />
        <span>{{ item.title }}</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "thisThree",
  data() {
    return;
  },
  props: {
    recommend: [],
  },
};
</script>

<style>
.thisThree {
  display: flex;
  height: 150px;
  width: 100%;
  /* background-color: rgb(126, 226, 122); */
  text-align: center ;
  border-bottom : 10px solid #eee;
}
.threetwo {
  padding-top: 10px;
  flex: 1;
  /* background-color: ; */
}
.threetwo img {
  width: 85%;
  /* height: 85%; */
}
</style>