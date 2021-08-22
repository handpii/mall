<template>
  <!-- <swiper ref="swiper" v-if="banners.length" >
    <swiper-item v-for="(item, index) in banners" :key="item.index">
      <a :href="item.link">
        <img :src="item.image" alt="" @load="imageLoaded">
      </a>
    </swiper-item>
  </swiper> -->
    <div class="HomeSwiper">
    <!-- <span class="demonstration">默认 Hover 指示器触发</span> -->

  <el-carousel  height="196px">
    <el-carousel-item v-for="(item) in banners" :key="item.index">
         <a :href="item.link">
        <img :src="item.image" alt="" @load="imageLoaded">
      </a>
    </el-carousel-item>
  </el-carousel>
  </div>
</template>

<script>
import { Swiper, SwiperItem } from "@/components/common/swiper";

export default {
  name: "HomeSwiper",
  props: {
    banners: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      isLoaded: false,
    };
  },
  components: {
    Swiper,
    SwiperItem,
  },
  methods: {
    startTimer() {
      this.$refs.swiper && this.$refs.swiper.startTimer();
    },
    stopTimer() {
      this.$refs.swiper && this.$refs.swiper.stopTimer();
    },
    imageLoaded() {
      if (!this.isLoaded) {
        this.$emit("swiperLoaded");
        this.isLoaded = true;
      }
    },
  },
};
</script>

<style scoped>
.el-carousel__item img {
  width: 100%;
}
.el-carousel__item {
  height: 196px;
}

.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 196px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>