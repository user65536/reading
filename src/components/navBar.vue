<template>
  <div class="wrapper-nav-bar">
    <div class="nav">
      <div @click="navbarChange(0)" class="nav-item" :class="activeIndex == 0 ? 'active' : ''">
        <span class="iconfont icon-shu"></span>
        <div class="name">图书</div>
      </div>
      <div @click="navbarChange(1)" class="nav-item" :class="activeIndex == 1 ? 'active' : ''">
        <span class="iconfont icon-wode"></span>
        <div class="name">我的</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      
    }
  },
  props: ['activeIndex'],
  methods: {
    navbarChange(index) {
      this.$emit("navbarChange", index)
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper-nav-bar
  position fixed
  bottom 0
  left 0
  right 0
  .nav
    height 48px
    display flex
    justify-content space-between
    .nav-item
      flex 1 1 50%
      display flex
      flex-direction column
      justify-content center
      align-items center
      color #c3c3c3
      &.active
        color #82c89b
      .iconfont
        font-size 20px
      .name 
        font-size 14px
        text-align center
      
    
</style>