<template>
  <div class="muchdate">
    <muchdata-item
      v-for="items in muchdataarr"
      :goodsItem="items"
      :key="items.iid"
      class="item"
    ></muchdata-item>
  </div>
</template>

<script>
import muchdataItem from "./muchdataItem.vue";

export default {
    name: "muchdate",
  components: {
    muchdataItem,
  },
  props: {
    muchdataarr: {
      type: Array,
      default() {
        return [];
      },
    },
  },
};
</script>

<style>
  .muchdate {
    display: flex;
    flex-wrap: wrap;
    padding: 5px;
    justify-content: space-around;
  }

  .muchdate .item {
    width: 48%;
  }

</style>