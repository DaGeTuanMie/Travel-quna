<template>
    <div class="header">
      <div class="header-left"><div class="iconfont icon1">&#xe696;</div></div>
      <div class="header-input"><i class="iconfont icon2">&#xe60b;</i>输入城市/游玩/主题</div>
      <div class="header-right">城市<i class="iconfont icon3">&#xe60c;</i></div>
    </div>
</template>

<script>
    export default {
        name: "HomeHeader"
    }
</script>

<style scoped lang="stylus">
  @import "~@/assets/styles/varibles.styl"
  .header
    display flex
    line-height .86rem
    color #ffffff
    background $bgColor
    .header-left
      width .64rem
      float left
      .icon1
        font-size .4rem
        text-align center
    .header-input
      flex 1
      height .64rem
      line-height .64rem
      padding-left .2rem
      margin-top .12rem
      margin-left .2rem
      background #ffffff
      color #ccc
      border-radius .1rem
    .header-right
      width 1.24rem
      float right
      text-align center
      .icon3
        vertical-align top
        font-size .24rem
</style>
