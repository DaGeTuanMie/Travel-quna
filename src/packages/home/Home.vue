<template>
    <div class="home">
      <div class="box">
        <home-header></home-header>
        <home-swiper></home-swiper>
      </div>
    </div>
</template>

<script>
  import HomeHeader from './components/Header'
  import HomeSwiper from './components/Swiper'
    export default {
        name: "Home",
        components:{
          HomeHeader,
          HomeSwiper
        }
    }
</script>

<style scoped>
</style>
