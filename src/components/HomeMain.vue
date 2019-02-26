<template>
  <div class="home-main">
    <SideComponent/>
    <div class="home-main-bg">
        <div class="home-main-bg-wrp">
          <img src="@/assets/bg.png" alt="">
        </div>
      </div>
    <div class="home-main-section-top">
      <div class="home-main-banner">
        <img src="@/assets/c-mask.png" alt="">
      </div>
      <div class="hero-text">
        <div class="hero-text-line">CLOUD</div>
        <div class="hero-text-line">EXPERIENCE</div>
        <div class="hero-text-line">DESIGN</div>
      </div>
    </div>
    <div class="home-main-section-inner-nav">
      <h2>CXD FAMILY</h2>
      <div class="cadr-contant">
        <div class="card">
          <img src="@/assets/pic1.png" alt="">
          <h4>CXD·规范</h4>
          <p>一套服务百度云业务的设计规范</p>
          <a href="#">READ MORE</a>
        </div>
        <div class="card-col-mask"></div>
        <div class="card">
          <img src="@/assets/pic2.png" alt="">
          <h4>CXD·规范</h4>
          <p>一套服务百度云业务的设计规范</p>
          <a href="#">READ MORE</a>
        </div>
        <div class="card-col-mask"></div>
        <div class="card">
          <img src="@/assets/pic3.png" alt="">
          <h4>CXD·规范</h4>
          <p>一套服务百度云业务的设计规范</p>
          <a href="#">READ MORE</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SideComponent from '@/components/SideComponent.vue'
export default {
  components: {
    SideComponent
  }
}
</script>


<style lang="stylus">
.home-main
  min-height 800px
  // 背景
  .home-main-bg
    position fixed
    top 0
    left 0
    bottom 0
    right 0
    z-index -1
    .home-main-bg-wrp
      max-width 1070px
      margin auto 
      overflow hidden
      img 
        height 100%
  // 顶部板块
  .home-main-section-top
    margin 70px 0 0 0
    position relative
    height 740px
    &:before
      content ""
      display block
      width 100%
      height 120px
      position absolute
      top -120px
      left 0
      background-color #fff
    // banner 图
    .home-main-banner
      width 1080px
      margin auto 
      img 
        width 100%
    // 文字
    .hero-text
      position absolute
      width 770px
      left 50%
      transform translateX(-50%)
      top 340px
      .hero-text-line  
        display block
        width fit-content
        width -webkit-fit-content
        width -moz-fit-content
        height 80px
        line-height 80px
        font-size 72px
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
  //第二个板块
  .home-main-section-inner-nav
    width 1080px
    margin auto
    height 700px
    position relative
    // mask
    &:before
      width 100%
      height 198px
      position absolute
      content ""
      display block
      background-color #fff
      z-index -1
      top -104px
    &:after
      width 100%
      height 360px
      position absolute
      content ""
      display block
      background-color #fff
      z-index -1
      bottom 0px  
    h2
      font-family "avenir", "PingFang SC", "SF Pro SC","SF Pro Text","Helvetica Neue",  Helvetica,  Roboto, 'Arial','microsoft yahei ui',"Microsoft YaHei",SimSun, sans-serif;
      -moz-osx-font-smoothing grayscale
      -webkit-font-smoothing antialiased
      font-size 23px
      line-height 33px
      font-weight 900
      margin 40px 0 60px
      text-align center
    // 卡片
    .card-col-mask
      float left
      width 180px
      height 410px
      background-color #fff
    .card 
      width 240px
      height 410px
      float left
      &:hover
        cursor pointer
      img 
        width 100%
      h4
        margin-top 35px
        margin-bottom 0px
        font-size 24px
        line-height 38px
        color #3A3A3A
      p
        font-size 14px
        line-height 26px
        color #3A3A3A
        margin-top 10px
        margin-bottom 0px
      a
        display block
        font-size 12px
        line-height 24px
        height 34px
        margin-top 15px
        margin-bottom 0px
        width 120px
        font-family "avenir", "PingFang SC", "SF Pro SC","SF Pro Text","Helvetica Neue",  Helvetica,  Roboto, 'Arial','microsoft yahei ui',"Microsoft YaHei",SimSun, sans-serif;
        -moz-osx-font-smoothing grayscale
        -webkit-font-smoothing antialiased
        color #3A3A3A
        font-weight 900
        position relative
        letter-spacing 3px
        &:after
          content ""
          display block
          height 3px
          position absolute
          bottom -5px
          left 0
          width 35px
          background-color #000




</style>


