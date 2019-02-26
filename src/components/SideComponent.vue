<template>
    <div class="cxd-side-component">
        <div class="left">
            CLOUD EXPERIENCE DESIGN
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
    transform rotate(-90deg) translateY(-50%)
    top 50%
    left -40px
  .right
    position fixed
    z-index 99
    font-weight 900
    right 20px
    transform translateY(-50%)
    top 50%
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

