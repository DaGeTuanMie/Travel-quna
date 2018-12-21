<template>
  <div class="weekend">
    <div class="recommend-title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item of weekendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "HomeWeekend",
    data(){
      return{
        weekendList:[
          {
            id:"0001",
            imgUrl:"http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg",
            title:"大连圣亚海洋世界",
            desc:"浪漫大连首站，浪漫的海洋主题乐园"
          },{
            id:"0002",
            imgUrl:"http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg",
            title:"大连圣亚海洋世界",
            desc:"浪漫大连首站，浪漫的海洋主题乐园"
          },{
            id:"0003",
            imgUrl:"http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg",
            title:"大连圣亚海洋世界",
            desc:"浪漫大连首站，浪漫的海洋主题乐园"
          },{
            id:"0004",
            imgUrl:"http://img1.qunarzz.com/sight/source/1510/6e/1ea71e2f04e.jpg_r_640x214_aa6f091d.jpg",
            title:"大连圣亚海洋世界",
            desc:"浪漫大连首站，浪漫的海洋主题乐园"
          }
        ]
      }
    }
  }
</script>

<style scoped lang="stylus">
  @import "~@/assets/styles/minins.styl"
  .recommend-title
    line-height .4rem
    background #ccc
    text-indent .2rem
    margin-top .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    min-width 0
    .item-title
      line-height .54rem
      font-size .32rem
      ellipse()
    .item-desc
      line-height .4rem
      color #ccc
      ellipse()
</style>

