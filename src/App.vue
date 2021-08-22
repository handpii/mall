<template>
  <div id="app">
    
    <router-view></router-view>
    <tabbarzi/>
  </div>
</template>

<script>
import tabbarzi from './components/tabbar/tabbarzi.vue'

// import tabbarzi from ''

export default {
  name: 'App',
  components: {
    tabbarzi
   
  }
}
</script>

<style>
  @import "assets/css/base.css";
  @import "assets/css/normalize.css";
</style>
