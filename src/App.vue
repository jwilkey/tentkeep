<template>
  <div id="app" class="theme-back">
    <router-view class="vfull scrolly noscrollx"/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="less">
@import "../static/tentkeep-styles/common";
html, body, #app {
  height: 100%;
  margin: 0;
  overflow: hidden;
}
.noscrollx {
  overflow-x: hidden;
}
</style>
