<template>
  <div class="recommend">
    <ul class="listitem-con border-top">
      <li class="listentrance-item border-right">定位失败</li>
      <li class="listentrance-item">玩水季</li>
    </ul>
    <ul class="activity-con border-top">
      <li class="activity-item border-right"></li>
      <li class="activity-item activity-item-two"></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend'
}
</script>

<style lang='stylus' scoped>
.recommend {
  .listitem-con {
    width: 100%;
    background-color: #fff;
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: box;
    width: 100%;
    background-color: #fff;

    .listentrance-item {
      -webkit-box-flex: 1;
      -moz-box-flex: 1;
      -ms-flexbox-flex: 1;
      box-flex: 1;
      overflow: hidden;
      width: 0;
      height: 0.98rem;
      font-size: 0.28rem;
      color: #212121;
      line-height: 0.98rem;
      text-align: center;
    }
  }

  .activity-con {
    display: -webkit-box;
    display: -moz-box;
    display: -ms-flexbox;
    display: box;
    width: 100%;
    margin-top: 0.2rem;
    background-color: #fff;

    .activity-item {
      -webkit-box-flex: 1;
      -moz-box-flex: 1;
      -ms-flexbox-flex: 1;
      box-flex: 1;
      box-flex: 1;
      position: relative;
      width: 0;
      height: 1.4rem;
      line-height: 1.4rem;
      color: #212121;
      font-size: 0.28rem;
      background: url('http://img1.qunarzz.com/piao/fusion/1806/29/30427c0e0658b502.png') center center no-repeat;
      background-size: auto 100%;
    }

    .activity-item-two {
      background: url('http://img1.qunarzz.com/piao/fusion/1809/b7/00000ce26b312902.png') center center no-repeat;
      background-size: auto 100%;
    }
  }
}
</style>
