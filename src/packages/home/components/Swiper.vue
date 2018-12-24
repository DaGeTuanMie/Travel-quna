<template>
    <div class="swiper">
      <swiper :options="swiperOption" ref="mySwiper" v-if="swiperList.length">
        <!-- slides -->
        <swiper-slide v-for="item of swiperList" :key=item.id>
          <img class="swiper-img" :src="item.imgUrl">
        </swiper-slide>
        <!-- Optional controls -->
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
</template>

<script>
    export default {
        name: "HomeSwiper",
        props:{
          swiperList:Array
        },
        data(){
          return{
            swiperOption:{
              pagination:'.swiper-pagination',
              loop:true
            }
          }
        }
    }
</script>

<style scoped lang="stylus">
  .swiper >>> .swiper-pagination-bullet-active
    background #ffffff
  .swiper
    overflow hidden
    width 100%
    height 0
    padding-bottom 26.7%
    .swiper-img
      width 100%
</style>
