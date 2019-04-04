<template>
  <div class="wrapper-recommend">
    <div class="preview">
      <div class="cover">
        <img class="img" src="http://open.6api.net/mpic/s11284102.jpg" alt="">
      </div>
      <div class="title">霍乱时期的爱情</div>
      <div class="author">加西亚·马尔克斯</div>
    </div>
    <div class="input-wrap">
      <div class="lable">ISBN:</div>
      <div class="input-bar">
        <input class="input" type="text">
        <span class="iconfont icon-saoma"></span>
      </div>
    </div>
    <div class="btn-wrap">
      <div @click="showModal" class="btn btn-search">查询</div>
      <div @click="showModal" class="btn btn-recommend">推荐</div>
    </div>
    <div @click="showModal" class="tips">信息不准确?联系我们</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      
    }
  },
  methods: {
    showModal() {
      mpvue.showModal({
        title: '还没写~~~'
      })
    }
  }
}
</script>

<style lang="stylus" scoped>
@import './recommend.styl'
</style>