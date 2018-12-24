<template>
    <div class="header">
      城市选择
      <router-link to="/">
        <div class="iconfont header-icon">&#xe696;</div>
      </router-link>
    </div>
</template>

<script>
    export default {
        name: "CityHeader"
    }
</script>

<style scoped lang="stylus">
  @import "../../../assets/styles/varibles.styl"
  .header
    position relative
    overflow hidden
    height .86rem
    line-height .86rem
    text-align center
    color #ffffff
    background $bgColor
    font-size .32rem
    .header-icon
      position absolute
      top 0
      left 0
      width .64rem
      color #ffffff
      text-align center
      font-size .4rem
</style>
