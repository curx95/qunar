<template>
  <div class="hotlist">
    <div class="hotlist-group">
      <img class="hotlist-title-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" alt="本周热门榜单"><span class="hotlist-title-text">本周热门榜单</span>
      <a class="hotlist-title-more" href="http://touch.piao.qunar.com/touch/weekHotSales.htm?cityName=杭州">全部榜单
        <span>❯</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHotList'
}
</script>

<style lang="stylus" scoped>
  .hotlist
    background #fff
    margin-top .2rem
    .hotlist-group
      background none !important
      position relative;
      padding .24rem 0 .26rem;
      .hotlist-title-img
        display: inline-block;
        overflow: hidden;
        width: .3rem;
        height: .3rem;
        margin-left: .2rem;
        vertical-align: top;
      .hotlist-title-text
        display: inline-block;
        margin-left: .08rem;
        height: .44rem;
        color: #212121;
        font-size: .32rem;
        line-height: .44rem;
      .hotlist-title-more
        position: absolute;
        top: .36rem;
        right: .32rem;
        color: #616161;
        font-size: .24rem;
        line-height: .28rem;
</style>
