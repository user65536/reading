<template>
  <div class="wrapper-detail">
    <div class="cover-area">
      <div class="cover-wrap">
        <div class="cover">
          <img src="http://open.6api.net/mpic/s11284102.jpg" alt="" class="img">
        </div>
        <div class="shadow"></div>
      </div>
    </div>
    <div class="content">
      <div class="title">霍乱时期的爱情</div>
      <div class="author">加西亚·马尔克斯</div>
      <div class="intro">《霍乱时期的爱情》是加西亚•马尔克斯获得诺贝尔文学奖之后完成的第一部小说。讲述了一段跨越半个多世纪的爱情史诗，穷尽了所有爱情的可能性：忠贞的、隐秘的、粗暴的、羞怯的、柏拉图式的、放荡的、转瞬即逝的、生死相依的……再现了时光的无情流逝，被誉为“人类有史以来最伟大的爱情小说”，是20世纪最重要的经典文学巨著之一。</div>
    </div>
    <div class="bottom-tool">
      <div @click="changeLike" class="like">
        <span class="iconfont" :class="like ? 'icon-xiangkan' : 'icon-xihuan'"></span>
        <span class="num">1242</span>
      </div>
      <div @click="showModal" class="share">
        <span class="iconfont icon-fenxiang"></span>
        <span class="name">分享</span>
      </div>
      <div @click="showModal" class="btn">上架提醒</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      like: false
    }
  },
  methods: {
    changeLike() {
      this.like = !this.like
    },
    showModal() {
      mpvue.showModal({
        title: '还没写~~~'
      })
    }
  }
}
</script>

<style lang="stylus" scoped>
@import './detail.styl'
</style>