<template>
  <div class="home" :class="[isFirstPage? 'first-page': '']">
    <SideComponent/>
    <HomeMainFullPage/>
    <div class="home-after-main">
      <HomeCard/>
      <!-- 插槽 -->
      <slot></slot> 
    </div>
    <!-- 背景视频 -->
    <div class="home-bg">
      <video src="https://cxd-public.cdn.bcebos.com/cxd-guide/bg.mp4" autoplay="autoplay" muted loop/>
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
  },
  computed: {
    // 浏览器高度
    browserHeight() {
      return document.documentElement.clientHeight
    }
  },
  data() {
    return {
      scrollPosition : 0,
      isScroll : false,
      isFirstPage : true,
    }
  },
  created() {
    this.scrollBack();
  },
  mounted(){
      this.scrollBack();
      window.addEventListener('scroll',this.handleScroll,true)
   },
  methods: {
     scrollBack() {
       document.body.scrollTop = 0
       document.documentElement.scrollTop = 0
       window.pageYOffset = 0
     },
     handleScroll(e){
       var scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop;
       // 判断上还是下
       var i = scrollTop - this.scrollPosition;
       this.scrollPosition = scrollTop;
       // 判断是否在首屏
       var firstPageHeight = this.browserHeight
       if(this.isFirstPage) {
         if (i > 0) {
           //setTimeout(()=>{this.isFirstPage = false;},500);
         }
       }
       if(!this.isFirstPage) {
         if (scrollTop === 0) {
           if (i < 0) {
              //setTimeout(()=>{this.isFirstPage = true;},500);
           }
         }
       }
     },

  }
}

</script>

<style lang="stylus">
  .home.first-page
    .home-after-main
      top 100%
  .home
    height 100%
    width 100%
    position relative
    .home-after-main
      transition all 1s cubic-bezier(0.11, 0.73, 0.24, 0.98) //首屏动画
      //height 100%
      width 100%
      position absolute
      top 0
      //transform translateY(100%)
  .home-bg
    width 100%
    height 100%
    background-color #fff
    position fixed
    top 0
    z-index -1
    overflow hidden
    video 
      height 100%
</style>

