 <template>
  <div class="tabcontrol">
    <div class="tabcontrolitem" v-for="(item,index) in list" 
    :class="{active:currentIndex===index}" @click="tanconClick(index)" :key="item">
      <span>{{ item }}</span>
    </div>
  </div>
</template>


<script>
export default {
  name: "tabcontrol",
  props: {
    list: {
      type: Array,
      default() {
        return ["流行", "新款", "精选"];
      },
    },
  },
  data() {
    return {
      currentIndex: 0,
    };
  },
  methods: {
    tanconClick(index){
   this.currentIndex=index;
   this.$emit("tabClick",index)
    }
  },
};
</script>


<style scoped>
  .tabcontrol {
    display: flex;
    text-align: center;
    line-height: 40px;
    font-size: 15px;
    background-color: #fff;
        position: sticky;
    top: 44px;
    z-index: 99;
  }

  .tabcontrolitem {
    flex: 1;

  }

  .tabcontrolitem span {
    padding: 5px;
  }

  .active {
    color: var(--color-high-text);
  }

  .tabcontrolitem.active span {
    border-bottom: 2px solid var(--color-high-text);
  }
</style>