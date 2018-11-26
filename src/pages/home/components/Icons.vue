<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <div class="icon-dec">{{ item.dec }}</div>
        </div>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        autoplay: false
      },
      iconsData: [
        {
          id: '001',
          imgUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          dec: '景点门票'
        },
        {
          id: '002',
          imgUrl:
            'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          dec: '北京必游'
        },
        {
          id: '003',
          imgUrl:
            'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          dec: '一日游'
        },
        {
          id: '004',
          imgUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
          dec: '文化古迹'
        },
        {
          id: '005',
          imgUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
          dec: '动植物园'
        },
        {
          id: '006',
          imgUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/6c/9e54a8540fee0102.png',
          dec: '故宫'
        },
        {
          id: '007',
          imgUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png',
          dec: '野生动物园'
        },
        {
          id: '008',
          imgUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
          dec: '泡温泉'
        },
        {
          id: '008',
          imgUrl:
            'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
          dec: '泡温泉'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsData.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/variables.styl';

.icons >>> .swiper-container {
  height: 3.7rem;
  padding-top: 0.1rem;
  background-color: #fff;

  .icon {
    float: left;
    width: 25%;
    height: 1.5rem;
    padding-top: 0.1rem;
    text-align: center;

    .icon-img {
      display: inline-block;
      width: 1.1rem;
      height: 1.1rem;

      .icon-img-content {
        width: 1.1rem;
        height: 1.1rem;
        background: 0;
      }
    }

    .icon-dec {
      margin-top: 0.1rem;
      color: #212121;
      font-size: 0.28rem;
    }
  }
}
</style>
