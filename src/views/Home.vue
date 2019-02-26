<template>
  <div class="home">
    <SideComponent/>
    <HomeMainFullPage/>
    <div class="home-after-main">
      <HomeCard/>
      <!-- 插槽 -->
      <slot></slot> 
    </div>
    <!-- 背景图 -->
    <div class="home-bg">
      <img src="@/assets/bg.png" alt="">
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeMainFullPage from '@/components/HomeMainFullPage.vue'
import SideComponent from '@/components/SideComponent.vue'
import HomeCard from '@/components/HomeCard.vue'

export default {
  name: 'home',
  components: {
    HomeMainFullPage,
    SideComponent,
    HomeCard
  }
}
</script>

<style lang="stylus">
  .home
    height 100%
    width 100%
    position relative
    .home-after-main
      //height 100%
      width 100%
      position absolute
      top 100%
      //transform translateY(100%)
  .home-bg
    width 100%
    height 100%
    background-color #fff
    position fixed
    top 0
    z-index -1
    overflow hidden
</style>

