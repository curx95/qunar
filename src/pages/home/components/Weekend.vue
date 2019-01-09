<template>
  <div class="weekend">
    <h2 class="weekend-title">周末去哪儿</h2>
    <div v-for="item of WeekendData" :key="item.name" class="product-item">
      <a href="javascript:void 0" class="fulllink">
        <div class="product-imgcontainer">
          <img :src="item.img">
        </div>
        <div class="product-info">
          <p class="product-name">{{item.name}}</p>
          <p class="product-desc">{{item.desc}}</p>
        </div>
      </a>
    </div>
    <div class="price-desc">
      <div class="price-desc-info">
        <span class="price-desc-highlight">票面价</span>
        是指通过景区指定窗口售卖的纸质门票上标注的价格
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      WeekendData: [
        {
          img: 'http://img1.qunarzz.com/sight/source/1505/9f/7d45cc38259e0.jpg_r_640x214_156f4299.jpg',
          name: '承载杭城的历史之地',
          desc: '饱经沧桑的地方诉述着这座城的段段衷肠'
        },
        {
          img: 'http://img1.qunarzz.com/sight/source/1505/a3/9c9d78e925e8bc.jpg_r_640x214_74656d68.jpg',
          name: '泡汤好去处',
          desc: '泡在氤氲的温泉中，聆听冬天脚步的声音'
        },
        {
          img: 'http://img1.qunarzz.com/sight/source/1510/c1/afe3ab32b3bc23.jpg_r_640x214_beb61760.jpg',
          name: '青山秀水，精致暖汤',
          desc: '天然高品质温泉，这个冬天秀美容颜首选'
        },
        {
          img: 'http://img1.qunarzz.com/sight/source/1811/52/b6776b49d27025.jpg_r_640x214_35ae205c.jpg',
          name: '美丽普陀山',
          desc: '人间仙境杭州，佛教圣地普陀山等你来玩'
        },
        {
          img: 'http://img1.qunarzz.com/sight/source/1509/fb/c45a951a9b4305.jpg_r_640x214_26fcfd26.jpg',
          name: '温州动人秋色',
          desc: '细数温州那些美到陶醉的赏秋地'
        }
      ]
    }
  }
}
</script>

<style scoped lang="stylus">
.weekend {
  .weekend-title {
    height: 0.8rem;
    padding-left: 0.26rem;
    line-height: 0.8rem;
    color: #212121;
  }

  .product-item {
    position: relative;
    margin-bottom: 0.1rem;
    background: #fff;

    .fulllink {
      display: block;
      width: 100%;
      height: 100%;

      .product-imgcontainer {
        overflow: hidden;
        height: 0;
        padding-bottom: 37.4375%;
        background-color: #dcdcdc;

        img {
          width: 100%;
          vertical-align: middle;
          border: 0;
        }
      }
    }
  }

  .product-info {
    position: relative;
    padding: 0.14rem 0.2rem 0.2rem 0.2rem;

    .product-name {
      overflow: hidden;
      padding-right: 1.4rem;
      color: #212121;
      font-size: 0.28rem;
      line-height: 0.48rem;
      white-space: nowrap;
      text-overflow: ellipsis;
    }

    .product-desc {
      overflow: hidden;
      padding-right: 1.4rem;
      color: #616161;
      font-size: 0.24rem;
      line-height: 0.48rem;
      white-space: nowrap;
      text-overflow: ellipsis;
    }
  }

  .price-desc {
    margin-top: 0.1rem;
    padding: 0.14rem 0.1rem;
    font-size: 0.24rem;
    line-height: 0.32rem;
    background: #fff;
    color: #616161;
    .price-desc-info {
      margin-left .3rem
      .price-desc-highlight{
        font-weight bold
      }
    }
  }
}
</style>
