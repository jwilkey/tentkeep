<template>
  <div class="titlebar flex-row align-center">
    <img @click="goHome" src="../../static/images/logo.png" />
    <p @click="goHome" class="marginl">TENTKEEP</p>
  </div>
</template>

<script>
export default {
  name: 'titlebar',
  data () {
    return {
    }
  },
  methods: {
    goHome () {
      this.$router.push('/')
    }
  }
}
</script>

<style lang="less" scoped>
.titlebar {
  padding: 8px;
  img {
    cursor: pointer;
    height: 30px;
  }
}
</style>
