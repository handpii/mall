<template>
  <div class="wraper" ref="aaa">
    <div class="common">
      <slot></slot>
    </div>
  </div>
</template>

<script>
import BScroll from "better-scroll";

export default {
  data() {
    return {
      scroll: null,
    };
  },
  props: {
    probeType:{
      type:Number,
      default:0
    },
    click:{
      type:Boolean,
      default:false
    },
    pullUpLoad:{
      type:Boolean,
      default:false
    }
  },
  //  不能使用create创建，用create取不到this值
  mounted() {
    this.scroll = new BScroll(this.$refs.aaa, {
      probeType: this.probeType,
      click: this.click,
      pullUpLoad:this.pullUpLoad  
    });
    this.scroll.on('scroll',(position)=>{
      // console.log(position);
      this.$emit('scroll',position)
    })
      this.scroll.on('pullingUp',()=>{
      // console.log("position");
      this.$emit('pullingUp')
    })
  },

  methods: {
    refresh() {
      // this.scroll && this.scroll.refresh && this.scroll.refresh()
      this.scroll.refresh()
    },
    

  },
    watch: {
      data() {
	      setTimeout(this.refresh, 20)
      }
    }
};
</script>

<style>
.wraper {
  /* height: 100%; */
  /* background-color: #63ec13; */
  overflow: hidden;
}
</style>