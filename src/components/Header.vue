<template>
    <div class="cxd-header">
        <Nav @toggle-nav="toggleNav()"/>
        <img alt="logo" class="logo" src="@/assets/logo.png">
        <div class="header-humberger" 
          :class="isNavOpen()"
          @click="toggleNav()">
            <span class="humberger-ele top"></span>
            <span class="humberger-ele mid"></span>
            <span class="humberger-ele bottom"></span>
        </div>
    </div>
</template>

<script>
import Nav from '@/components/Nav.vue'
export default {
    components: {
        Nav
    },
    methods : {
        isNavOpen() {
            if (this.$store.state.isNavOpen) {
                return "nav-open"
            } else {
                return "nav-close"
            }
        },
        toggleNav() {
            this.$store.state.isNavOpen = !this.$store.state.isNavOpen
        }
    }
}
</script>


<style lang="stylus">
  //  顶部导航栏全局样式
  .cxd-header
    z-index 100
    width 100%
    height 122px
    position fixed // 导航栏定位
    top 0
    left 0
    // 顶部导航栏的 logo
    .logo
      height 20px
      position absolute
      top 50%
      transform translateY(-50%)
      margin-left 40px // 左侧位置  
      z-index 3
    // 汉堡菜单组件
    .header-humberger
      z-index 3
      position absolute 
      top 50%
      right 40px
      transform translateY(-50%)
      width 15px
      height 14px 
      &:hover
        cursor pointer
      .humberger-ele
        display block
        width 15px
        height 2px
        border-radius 4px
        background-color #000
        margin-bottom 4px
      &.nav-open .humberger-ele
        &.top
          transform rotate(45deg) translate(4.3px,4.3px)
        &.mid
          transform scaleX(0)
        &.bottom
          transform rotate(-45deg) translate(4.3px,-4.3px)
</style>

