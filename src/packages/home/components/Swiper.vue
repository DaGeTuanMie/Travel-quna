<template>
    <div class="swiper">
      <swiper :options="swiperOption" ref="mySwiper">
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
        data(){
          return{
            swiperOption:{
              pagination:'.swiper-pagination',
              loop:true
            },
            swiperList:[{
              id:'0001',
              imgUrl:"http://img1.qunarzz.com/piao/fusion/1812/a8/33a03fe1c213da02.jpg_750x200_dd491fc5.jpg"
            },{
              id:'0002',
              imgUrl:"http://img1.qunarzz.com/piao/fusion/1812/92/edb99066ecb8ac02.jpg_750x200_059678c3.jpg"
        }]
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
