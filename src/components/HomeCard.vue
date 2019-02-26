<template>
  <div class="home-card">
    <h2>CXD FAMILY</h2>
    <div class="home-card-inner">
        <div class="left"></div>
        <div class="content">
          <div class="card">
              <img src="@/assets/pic1.png" alt="">
              <div class="bottom">
                <h4>CXD·规范</h4>
                <p>一套服务百度云业务的设计规范</p>
                <a href="#">READ MORE</a>
              </div>
          </div>
          <div class="mask"></div>
          <div class="card">
              <img src="@/assets/pic2.png" alt="">
              <div class="bottom">
                <h4>CXD·规范</h4>
                <p>一套服务百度云业务的设计规范</p>
                <a href="#">READ MORE</a>
              </div>
          </div>
          <div class="mask"></div>
          <div class="card">
              <img src="@/assets/pic3.png" alt="">
              <div class="bottom">
                <h4>CXD·规范</h4>
                <p>一套服务百度云业务的设计规范</p>
                <a href="#">READ MORE</a>
              </div>
          </div>
        </div>
        <div class="right"></div>
    </div>
  </div>
</template>

<style lang="stylus">
  .home-card-inner
    overflow hidden
    display flex
    .left,.right
      width 20%
      max-width 160px
      min-width 80px
      background-color #fff
    .content
      -webkit-box-flex 1
      flex 1 
      display flex
      .card
        max-width 220px
        width 26%  
        img 
          width 100%  
          display block  
        .bottom
          padding-left 16px
          background-color #fff 
      .mask
        -webkit-box-flex 1
        flex 1 
        background-color #fff

//文字

.home-card 
      h2
        font-family "avenir", "PingFang SC", "SF Pro SC","SF Pro Text","Helvetica Neue",  Helvetica,  Roboto, 'Arial','microsoft yahei ui',"Microsoft YaHei",SimSun, sans-serif;
        -moz-osx-font-smoothing grayscale
        -webkit-font-smoothing antialiased
        font-weight 900
        display block
        background-color #fff
        font-size 24px
        line-height 33px
        text-align center
        margin 0
        padding 60px 0
        color #333333

      h4
        padding-top 35px
        margin 0
        padding-bottom 0px
        font-size 24px
        line-height 38px
        color #3A3A3A
      p
        font-size 14px
        margin 0
        line-height 26px
        color #3A3A3A
        padding-top 10px
        padding-bottom 0px
      a
        display block
        margin 0
        font-size 12px
        line-height 24px
        height 34px
        padding-top 15px
        padding-bottom 10px
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
          bottom 5px
          left 0
          width 35px
          background-color #000
</style>

