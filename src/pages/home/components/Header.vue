<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont search-icon">&#xe632;</span>
      输入城市/游玩/主题</div>
    <div class="header-right">
      城市<span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .header
    display flex
    line-height .86rem
    background-color $bgColor
    color #fff
    .header-left
      .back-icon
        text-align center
        font-size .4rem
      width .64rem
      float left
    .header-input
      flex 1
      line-height .62rem
      border-radius .1rem
      background-color #fff
      margin-top .12rem
      margin-left .2rem
      padding-left 0.2rem
      height .62rem
      color #ccc
    .header-right
      .arrow-icon
        font-size .24rem
      width 1.24rem
      float right
      text-align center
</style>
