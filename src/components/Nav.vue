<template>
  <transition name="nav">
    <div class="cxd-nav" 
      v-show="this.$store.state.isNavOpen"
      @click="toggleNav()">
        <div class="nav-content">
          <a href="http://v3.yunshe.design" style="transition-delay:.05s;">CXD·规范</a>
          <a href="http://img.yunshe.design" style="transition-delay:.1s;">CXD·资源</a>
          <a href="#" style="transition-delay:.15s;">CXD·云舍 <span>(敬请期待)</span></a>
        </div>
    </div>
  </transition>
</template>

<script>
export default {
    methods: {
        toggleNav() {
            this.$emit("toggle-nav")
        }
    }
}
</script>


<style lang="stylus">
  .cxd-nav
    z-index 2
    position fixed
    top 0
    left 0
    right 0
    bottom 0
    background-color #fff
    // 导航
    .nav-content
      margin 90px auto
      width 140px
      overflow hidden
      padding-bottom 20px
      position relative
      &::after
        position absolute
        left 0
        bottom 0
        height 1px
        width 15px
        content " "
        display block
        background-color #000
    a
      display block
      font-size 14px
      line-height 20px
      margin 30px auto
      //text-align center
      font-weight bold
      color #000000
      transform translateY(0px)
      span 
        font-size 12px
        color #000
        font-weight normal
        opacity .5

//动画

.nav-enter
  opacity 0
  a
    transform translateY(30px)
    opacity 0
.nav-leave-to
  opacity 0
  a
    transform translateY(-30px)
    opacity 0
.nav-enter-active
  transition opacity .5s ease-in-out
  a
    transition all .5s ease-in-out 
.nav-leave-active
  transition opacity .5s ease-in-out .5s
  a
    transition all .5s ease-in-out 
</style>

