<template>
  <div id="app">
    <Header/>
    <router-view/>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'

export default {
  components: {
    Header
  }
}
</script>

<style lang="stylus">
  body
    margin 0
    padding 0
  a
    text-decoration-line none
  h1, h2, h3, h4, h5, p, a, span 
    font-family: -apple-system, BlinkMacSystemFont,"SF Pro SC","SF Pro Text","Helvetica Neue",  Helvetica, "PingFang SC", Roboto, 'Arial','microsoft yahei ui',"Microsoft YaHei",SimSun, sans-serif;
    /*修改浏览器渲染字体效果*/ 
    -moz-osx-font-smoothing: grayscale;  
    -webkit-font-smoothing: antialiased; 
</style>
