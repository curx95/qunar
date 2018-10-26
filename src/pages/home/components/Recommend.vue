<template>
  <ul class="listitem-con border-top">
    <li class="listentrance-item border-right">定位失败</li>
    <li class="listentrance-item">玩水季</li>
  </ul>
</template>

<script>
export default {
  name: 'HomeRecommend'
}
</script>

<style lang="stylus" scoped>
  .listitem-con
    width: 100%
    background-color: #fff
    display: -webkit-box
    display: -moz-box
    display: -ms-flexbox
    display: box
    width: 100%
    background-color: #fff
    .listentrance-item
      overflow hidden
      flex 1
      width: 0;
      height: .98rem;
      font-size: .28rem;
      color: #212121;
      line-height: .98rem;
      text-align: center;
</style>
