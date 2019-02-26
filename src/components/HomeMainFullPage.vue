<template>
  <div class="home-main-full-page">
      <div class="flex-content">
        <div class="mask left"></div>
        <div class="mid">
          <div class="top"></div>
          <div class="mask">
              <img src="@/assets/c-mask.png" alt="">
          </div>
          <div class="bottom"></div>
        </div>   
        <div class="mask right"></div> 
      </div>
      <div class="hero-text">
        <div class="hero-text-line">CLOUD</div>
        <div class="hero-text-line">EXPERIENCE</div>
        <div class="hero-text-line">DESIGN</div>
      </div>
  </div>
</template>

<style lang="stylus">
  .home-main-full-page
    width 100%
    height 100%
    position absolute
    top 0
    left 0
    .flex-content
      position absolute
      width 100%
      height 100%
      top 0
      left 0
      display flex
      justify-content center
    .mid, .mask
      height 100%
    .mid
      width 46%
      display flex
      flex-direction column
      .mask
        height fit-content
        height -webkit-fit-content
        height -moz-fit-content
        position relative
        img 
          width 100%
          display block  
      .top
        background-color #fff
        -webkit-box-flex 1
        flex 0.9
      .bottom  
        background-color #fff
        -webkit-box-flex 1
        flex 1    
    .left, .right
      background-color #fff
      -webkit-box-flex 1
      flex 1

.hero-text
  position absolute
  left 40%
  transform translateX(-50%)
  bottom 22%
  font-size 72px
  .hero-text-line  
    display block
    width fit-content
    width -webkit-fit-content
    width -moz-fit-content
    height 1.1em
    line-height 1.1em
    font-size 1em
    font-family "avenir", "PingFang SC", "SF Pro SC","SF Pro Text","Helvetica Neue",  Helvetica,  Roboto, 'Arial','microsoft yahei ui',"Microsoft YaHei",SimSun, sans-serif;
    -moz-osx-font-smoothing grayscale
    -webkit-font-smoothing antialiased
    font-weight 900
    position relative
    &::after
      position absolute
      left 0
      bottom 0
      height 7px
      width 100%
      content " "
      display block
      background-color #000
@media screen and (max-width: 1200px)
  .hero-text
    font-size 60px
@media screen and (max-width: 800px)
  .hero-text
    font-size 40px
    bottom 30%
    left 50%
</style>
</style>


