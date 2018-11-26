<template>
  <div class="mayyoulike">
    <div class="group-title">
      <img
        src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png"
        alt="猜你喜欢"
        class="title-img"
      >
      <span class="title">猜你喜欢</span>
    </div>
    <ul class="like-list">
      <li class="like-item border-bottom" v-for="item of LikeData" :key="item.title">
        <a class="fullLink" href="javascript:void 0">
          <div class="like-imgcon">
            <img class="like-img" :src="item.img" alt="">
          </div>
          <div class="like-tag">可定明日</div>
          <div class="like-info">
            <div class="like-title">{{ item.title }}</div>
            <div class="like-comment">
              <el-rate v-model="item.score" disabled text-color="#ff9900"></el-rate>
              <span class="comment-num">{{ item.commentNum }}</span>
            </div>
            <div class="like-price">
              <span class="price">
                ￥
                <em class="price-num">{{ item.price }}</em>
              </span>起
              <span class="address">{{ item.address }}</span>
            </div>
          </div>
        </a>
      </li>
    </ul>
    <a class="like-more border-top" href="javascript:void 0">查看所有产品</a>
  </div>
</template>

<script>
export default {
  name: 'HomeMayYouLike',
  data () {
    return {
      LikeData: [
        {
          img:
            'http://img1.qunarzz.com/sight/p0/1810/14/14b8a787d6e901f6a3.img.jpg_200x200_4a447e3c.jpg',
          title: '杭州云曼温泉',
          score: 4.7,
          commentNum: '972条评论',
          price: 125,
          address: '萧山区'
        },
        {
          img:
            'http://img1.qunarzz.com/sight/p0/1809/6b/6b0d71ae741a583da3.img.jpg_200x200_dc19cbb1.jpg',
          title: '杭州乐园',
          score: 4.9,
          commentNum: '9720条评论',
          price: 120,
          address: '萧山区'
        },
        {
          img:
            'http://img1.qunarzz.com/sight/p0/1411/b6/662fc49d1d26a5a7775cf6b7f8b4ecec.water.jpg_200x200_7dec115f.jpg',
          title: '杭州野生动物世界',
          score: 4.6,
          commentNum: '3572条评论',
          price: 125,
          address: '萧山区'
        },
        {
          img:
            'http://img1.qunarzz.com/sight/p0/201212/18/f195032e85740a4b93835fbb.jpg_200x200_77761d11.jpg',
          title: '杭州海底世界',
          score: 4.1,
          commentNum: '4972条评论',
          price: 160,
          address: '萧山区'
        },
        {
          img:
            'http://img1.qunarzz.com/sight/p0/1810/5e/5e855d32e9aff0aba3.img.jpg_200x200_a70a4170.jpg',
          title: '杭州烂苹果乐园',
          score: 4.0,
          commentNum: '4292条评论',
          price: 199,
          address: '萧山区'
        },
        {
          img:
            'http://img1.qunarzz.com/sight/p0/1709/28/288fbeccc335f774a3.img.jpg_200x200_4a81bde9.jpg',
          title: '“最忆是杭州”- G20峰会特别版《印象西湖》',
          score: 4.9,
          commentNum: '5972条评论',
          price: 220,
          address: '西湖'
        },
        {
          img:
            'http://img1.qunarzz.com/sight/p0/1508/12/4e6170303c63bdb7070fb1987480afab.water.jpg_200x200_0775a71c.jpg',
          title: '杭州极地海洋世界',
          score: 4.7,
          commentNum: '7202条评论',
          price: 299,
          address: '萧山区'
        }
      ]
    }
  }
}
</script>

<style lang='stylus'>
@import '~styles/mixins.styl';

.mayyoulike {
  margin-top: 0.2rem;
  background-color: #fff;

  .group-title {
    position: relative;
    padding: 0.24rem 0 0.26rem;

    .title-img {
      display: inline-block;
      overflow: hidden;
      width: 0.3rem;
      height: 0.3rem;
      margin-left: 0.2rem;
      vertical-align: top;
    }

    .title {
      display: inline-block;
      margin-left: 0.08rem;
      height: 0.44rem;
      color: #212121;
      font-size: 0.32rem;
      line-height: 0.44rem;
    }
  }

  .like-list {
    margin-left: 0.24rem;

    .like-item {
      position: relative;
      overflow: hidden;
      padding: 0.2rem 0;

      .fullLink {
        width: 100%;
        height: 100%;
        display: block;

        .like-imgcon {
          background-color: none !important;
          float: left;
          overflow: hidden;
          width: 2rem;
          height: 2rem;
          background-color: #f0f5f8;

          .like-img {
            width: 100%;
          }
        }

        .like-tag {
          background-image: url('https://img1.qunarzz.com/piao/fusion/1802/52/b9080e45b69b4f02.png');
          position: absolute;
          left: 0;
          top: 0.2rem;
          width: 1.02rem;
          height: 0.38rem;
          background-size: 100%;
          color: #fff;
          font-size: 0.2rem;
          line-height: 0.38rem;
          text-indent: 0.04rem;
        }
      }

      .like-info {
        overflow: hidden;
        padding-left: 0.22rem;

        .like-title {
          margin-top: 0.26rem;
          height: 0.44rem;
          color: #212121;
          font-size: 0.32rem;
          line-height: 0.44rem;
          ellipsis();
        }

        .like-comment {
          margin-top: 0.14rem;
          height: 0.34rem;
          font-size: 0.28rem;

          .el-rate {
            width: 1.5rem;
            height: 0.28rem;
            display: inline-block;

            .el-icon-star-on {
              font-size: 0.2rem;
              margin-right: 0.03rem;
            }
          }

          .comment-num {
            color: #616161;
            font-size: 0.24rem;
            line-height: 0.34rem;
            vertical-align: top;
          }
        }

        .like-price {
          margin-top: 0.22rem;
          position: relative;
          color: #616161;
          font-size: 0.24rem;
          line-height: 0.4rem;

          .price {
            color: #ff8300;

            .price-num {
              font-size: 0.4rem;
            }
          }

          .address {
            position: absolute;
            right: 0.24rem;
            bottom: 0;
          }
        }
      }
    }
  }

  .like-more {
    display: block;
    padding: 0.2rem 0;
    color: #00afc7;
    font-size: 0.28rem;
    line-height: 0.4rem;
    text-align: center;
  }
}
</style>
