<template>
  <div id="app" class="app">
    <v-header />
    <div class="tab">
      <div class="tab-item">
        <router-link to="/goods">商品</router-link>
      </div>
      <div class="tab-item">
        <router-link to="/ratings">评论</router-link>
      </div>
      <div class="tab-item">
        <router-link to="/seller">商家</router-link>
      </div>
    </div>
    <div class="content">
      <router-view/>
    </div>
  </div>
</template>

<script>
import vHeader from '@/components/header/Header'
export default {
  name: 'Home',
  components: {
    vHeader
  }
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
.app
  .tab
    display: flex
    width: 100%
    height: 1.066667rem
    line-height: 1.066667rem
    border-bottom: 1px solid rgba(7, 17, 27, 0.1)
    .tab-item
      flex: 1
      text-align: center
      & > a
        display: block
        font-size: 0.373333rem
        color: #535353
        text-decoration: none
        &.current
          color: #f56151
</style>
