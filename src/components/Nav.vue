<template>
    <div class="cxd-nav" 
      :class="isNavOpen()"
      @click="toggleNav()">
        <div class="nav-content">
          <a href="#">CXD·规范</a>
          <a href="#">CXD·资源</a>
          <a href="#">CXD·云舍</a>
        </div>
    </div>
</template>

<script>
export default {
    methods: {
        isNavOpen() {
            if (this.$store.state.isNavOpen) {
                return "nav-open"
            } else {
                return "nav-close"
            }            
        },
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
    &.nav-close
      display none
    // 导航
    .nav-content
      margin 90px auto
      width 80px
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
</style>

