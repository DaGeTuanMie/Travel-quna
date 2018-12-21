<template>
    <div class="recommend">
      <div class="recommend-title">热销推荐</div>
      <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
          <img class="item-img" :src="item.imgUrl">
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
        </li>
      </ul>
    </div>
</template>

<script>
    export default {
        name: "HomeRecommend",
        data(){
          return{
            recommendList:[
              {
                id:"0001",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1712/95/95f38f28a6ff19cba3.img.jpg_200x200_af967e35.jpg",
                title:"大连圣亚海洋世界",
                desc:"浪漫大连首站，浪漫的海洋主题乐园"
              },{
                id:"0002",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1712/95/95f38f28a6ff19cba3.img.jpg_200x200_af967e35.jpg",
                title:"大连圣亚海洋世界",
                desc:"浪漫大连首站，浪漫的海洋主题乐园"
              },{
                id:"0003",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1712/95/95f38f28a6ff19cba3.img.jpg_200x200_af967e35.jpg",
                title:"大连圣亚海洋世界",
                desc:"浪漫大连首站，浪漫的海洋主题乐园"
              },{
                id:"0004",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1712/95/95f38f28a6ff19cba3.img.jpg_200x200_af967e35.jpg",
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
  .item
    overflow hidden
    display flex
    height 1.9rem
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
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
      .item-button
        line-height .44rem
        margin-top .16rem
        background #ff9300
        color #ffffff
        padding 0 .2rem
        border-radius .06rem
</style>
