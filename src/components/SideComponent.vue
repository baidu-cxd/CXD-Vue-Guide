<template>
    <div class="cxd-side-component">
        <div class="left">
            CLOUD EXPERIENCE DESIGN
        </div>
        <div class="bottom">
            <span class="circle"></span>
        </div>
        <div class="right">
            <div class="weibo"></div>
            <span class="line"></span>
            <p>ABOUT</p>
        </div>
    </div>
</template>

<style lang="stylus">
.cxd-side-component
  .left
    font-size 12px
    position fixed
    z-index 99
    font-weight 900
    font-family "avenir", "PingFang SC", "SF Pro SC","SF Pro Text","Helvetica Neue",  Helvetica,  Roboto, 'Arial','microsoft yahei ui',"Microsoft YaHei",SimSun, sans-serif;
    -moz-osx-font-smoothing grayscale
    -webkit-font-smoothing antialiased
    transform rotate(-90deg)
    top 300px
    left -30px
  .bottom
    z-index 99
    position fixed
    width 1px
    height 50px
    background-color #000
    bottom 160px
    left 55px
    .circle
      width 10px
      height 10px
      background-color #000
      border-radius 100px
      position absolute
      top 0
      left -5px
  .right
    position fixed
    z-index 99
    font-weight 900
    right 40px
    top 300px
    .line
      width 2px
      height 45px
      display block
      background-color #000
      margin auto
    p
      font-size 12px
      transform rotate(90deg) translateX(15px)
      font-family "avenir", "PingFang SC", "SF Pro SC","SF Pro Text","Helvetica Neue",  Helvetica,  Roboto, 'Arial','microsoft yahei ui',"Microsoft YaHei",SimSun, sans-serif;
      -moz-osx-font-smoothing grayscale
      -webkit-font-smoothing antialiased
      font-weight 900
</style>

