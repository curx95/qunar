<template>
  <div class="hotlist">
    <div class="hotlist-group">
      <img class="hotlist-title-img" src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" alt="本周热门榜单"><span class="hotlist-title-text">本周热门榜单</span>
      <a class="hotlist-title-more" href="http://touch.piao.qunar.com/touch/weekHotSales.htm?cityName=杭州">全部榜单
        <span>❯</span>
      </a>
    </div>
    <ul class="hotsale-list" >
      <li class="hotsale-list-item" v-for="(item,index) of hotsaleList" :key='index'>
        <a class="funllink" href="javascript:void(0);">
          <div class="hotsale-list-tag" v-if="item.tagimg">
            <img class="hotsale-list-tagimg" :src=item.tagimg alt="">
          </div>
          <div class="hotsale-list-imgcon">
            <img class="hotsale-list-img" :src=item.img alt="">
          </div>
          <div class="hotsale-list-sight">{{item.sight}}</div>
          <div class="hotsale-list-price">
            <span class="hotsale-price" >¥<em class="hotsale-price-num">{{item.price}}</em></span>起
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeHotList',
  data () {
    return {
      hotsaleList:
      [
        {
          tagimg: 'http://img1.qunarzz.com/piao/fusion/1710/ab/159673b63e6ca702.png',
          img: 'http://img1.qunarzz.com/sight/p0/1411/b6/662fc49d1d26a5a7775cf6b7f8b4ecec.water.jpg_250x250_9d8a0a33.jpg',
          sight: '杭州野生动物世界',
          price: 170
        },
        {
          tagimg: 'http://img1.qunarzz.com/piao/fusion/1710/2d/36d0c4adaebbbc02.png',
          img: 'http://img1.qunarzz.com/sight/p0/1809/20/200086313333516ba3.water.jpg_250x250_a42f8860.jpg',
          sight: '杭州宋城景区',
          price: 0.1
        },
        {
          tagimg: 'http://img1.qunarzz.com/piao/fusion/1710/67/edc47ffef9e96b02.png',
          img: 'http://img1.qunarzz.com/sight/p0/1703/e3/e3d2c4a62fdc54aaa3.img.jpg_250x250_ad67cba7.jpg',
          sight: '灵隐寺',
          price: 45
        },
        {
          img: 'http://img1.qunarzz.com/sight/p0/1604/e3/e31e236ddd71e31b90.water.jpg_250x250_cdc2b480.jpg',
          sight: '梅峰岛',
          price: 100
        },
        {
          img: 'http://img1.qunarzz.com/sight/p0/1411/b6/662fc49d1d26a5a7775cf6b7f8b4ecec.water.jpg_250x250_9d8a0a33.jpg',
          sight: '杭州野生动物世界',
          price: 170
        },
        {
          img: 'http://img1.qunarzz.com/sight/p0/1411/b6/662fc49d1d26a5a7775cf6b7f8b4ecec.water.jpg_250x250_9d8a0a33.jpg',
          sight: '杭州野生动物世界',
          price: 170
        },
        {
          img: 'http://img1.qunarzz.com/sight/p0/1411/b6/662fc49d1d26a5a7775cf6b7f8b4ecec.water.jpg_250x250_9d8a0a33.jpg',
          sight: '杭州野生动物世界',
          price: 170
        },
        {
          img: 'http://img1.qunarzz.com/sight/p0/1411/b6/662fc49d1d26a5a7775cf6b7f8b4ecec.water.jpg_250x250_9d8a0a33.jpg',
          sight: '杭州野生动物世界',
          price: 170
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .hotlist
    background #fff
    margin-top .2rem
    .hotlist-group
      background none !important
      position relative
      padding .24rem 0 .26rem
      .hotlist-title-img
        display: inline-block
        overflow: hidden
        width: .3rem
        height: .3rem
        margin-left: .2rem
        vertical-align: top
      .hotlist-title-text
        display: inline-block
        margin-left: .08rem
        height: .44rem
        color: #212121
        font-size: .32rem
        line-height: .44rem
      .hotlist-title-more
        position: absolute
        top: .36rem
        right: .32rem
        color: #616161
        font-size: .24rem
        line-height: .28rem
    .hotsale-list
      padding: 0 .24rem
      overflow-x: scroll
      white-space: nowrap
      .hotsale-list-item
        position: relative
        display: inline-block
        padding: .06rem 0 .2rem
        width: 2rem
        &:not(:first-child)
          margin-left .12rem
        .funllink
          display: block
          width: 100%
          height: 100%
          .hotsale-list-tag
            position: absolute
            top: 0
            left: 0
            z-index: 1
            overflow: hidden
            width: .84rem
            height: .4rem
            .hotsale-list-tagimg
              width 100%
          .hotsale-list-imgcon
            overflow: hidden
            width: 2rem
            height: 0
            padding-bottom: 100%
            background: #f0f5f8
            .hotsale-list-img
              width 100%
          .hotsale-list-sight
            margin-top: .12rem
            color: #212121
            font-size: .24rem
            line-height: .32rem
            text-align: center
            ellipsis()
          .hotsale-list-price
            color: #616161;
            font-size: .24rem;
            line-height: .36rem;
            text-align: center;
            ellipsis()
            .hotsale-price
              color: #ff8300;
            .hotsale-price-num
              font-size: .28rem;
</style>
