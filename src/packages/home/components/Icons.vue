<template>
    <div class="icons">
      <swiper :options="swiperOption" ref="mySwiper">
        <swiper-slide v-for="(page,index) of pages" :key="index">
          <div class="icon" v-for="item of page" :key="item.id">
            <div class="icon-img">
              <img class="icon-img-content" :src="item.imgUrl">
            </div>
            <p class="icon-desc">{{item.desc}}</p>
          </div>
        </swiper-slide>
      </swiper>
    </div>
</template>

<script>
    import index from "../../../router";

    export default {
        name: "HomeIcons",
        data(){
          return{
            iconList:[
              {
                id:"0001",
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
                desc:"景点门票景点门票"
              },
              {
                id:"0002",
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
                desc:"景点门票"
              },
              {
                id:"0003",
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
                desc:"景点门票"
              },
              {
                id:"0004",
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
                desc:"景点门票"
              },{
                id:"0005",
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
                desc:"景点门票"
              },
              {
                id:"0006",
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
                desc:"景点门票"
              },
              {
                id:"0007",
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
                desc:"景点门票"
              },
              {
                id:"0008",
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
                desc:"景点门票"
              },
              {
                id:"0009",
                imgUrl:"http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
                desc:"北京必游"
              }
            ],
            swiperOption:{}
          }
        },
      computed:{
          pages(){
            const pages=[]
            this.iconList.forEach((item,index)=>{
              const page=Math.floor(index/8)
              if(!pages[page]){
                pages[page]=[]
              }
              pages[page].push(item)
            })
            return pages
          }
      }
    }
</script>

<style scoped lang="stylus">
  @import "~@/assets/styles/varibles.styl"
  @import "~@/assets/styles/minins.styl"
  .icons >>> .swiper-contaier
    width 100%
    height 0
    padding-bottom 50%
  .icon
    position relative
    overflow hidden
    float left
    height 0
    width 25%
    padding-bottom 25%
    .icon-img
      position absolute
      top 0
      right 0
      left 0
      box-sizing border-box
      padding .1rem
      bottom .44rem
      .icon-img-content
        display block
        margin 0 auto
        height 100%
    .icon-desc
      position absolute
      bottom 0
      right 0
      left 0
      height .44rem
      line-height .44rem
      text-align center
      color $darkTextColor
      ellipse()
</style>
