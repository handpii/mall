<template>
  <div class="top">
    <div class="left"><slot name="left"></slot></div>
    <div class="center"><slot name="center"></slot></div>
    <div class="right"><slot name="right"></slot></div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.top {
  display: flex;
  /* position: absolute; */
  height: 44px;
  text-align: center;
  /* background-color: rgb(14, 231, 50); */
}
.right {
  width: 44px;
  /* background-color: rgb(219, 137, 29); */
}
.left {
  /* position: relative; */
  /* display: block; */
  width: 40px;
  /* height: 42px; */
  /* background-color: rgb(219, 137, 29); */
}
.center {
  flex: 1;
}
</style>