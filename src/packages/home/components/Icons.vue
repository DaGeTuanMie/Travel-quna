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
        props:{
          iconList:Array
        },
        data(){
          return{
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
