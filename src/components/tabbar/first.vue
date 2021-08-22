<template>
    <div class="one">
    <slot></slot>

  </div>
</template>

<script>
export default {

}
</script>

<style>

body {
  border: 0;
  margin: 0;
}
.one {
  /* display: flex; */
    display: flex;
    background-color: #0bbedd;

    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;

}

</style>