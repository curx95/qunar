<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
    <home-hotList></home-hotList>
    <home-mayYouLike></home-mayYouLike>
    <home-weekend></home-weekend>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
import HomeRecommend from './components/Recommend'
import HomeHotList from './components/HotList'
import HomeMayYouLike from './components/MayYouLike'
import HomeWeekend from './components/Weekend'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeHotList,
    HomeMayYouLike,
    HomeWeekend
  }
}
</script>

<style lang="stylus" scoped>
.home {
  background-color: #f5f5f5;
}
</style>
