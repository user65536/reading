<template>
  <div class="wrapper-mine">
    <div class="card-area">
      <div class="card">
        <div class="info">
          <div class="ava">
            <img class="img" src="https://www.meansky.cn/picture/ava.jpg" alt="">
          </div>
          <div class="text">Trage Mo</div>
        </div>
        <div class="recommend">累计推荐图书 19 本</div>
      </div>
    </div>
    <div class="content">
      <div class="content-header">
        <div class="title">与我相关</div>
        <div class="tools">
          <div @click="showModal" class="tool-item">
            <span class="iconfont icon-bianji"></span>
            <span class="name">编辑</span>
          </div>
          <div @click="navigateToRecommend" class="tool-item">
            <span class="iconfont icon-add-line"></span>
            <span class="name">推荐</span>
          </div>
        </div>
      </div>
      <div class="books-wrap">
        <div @click="navigateToDetail" v-for="(book, index) in books" :key="index" class="book-item">
          <div class="cover">
            <img class="img" :src="book.images_medium" alt>
            <div class="bottom-mask">未上架</div>
          </div>
          <div class="title">{{book.title}}</div>
        </div>
      </div>
    </div>
    <nav-bar @navbarChange="navbarChange" :activeIndex="1"></nav-bar>
  </div>
</template>

<script>
import navBar from '@/components/navBar'
export default {
  data() {
    return {
      books: [
        {
          author: " 加西亚·马尔克斯",
          images_medium: "http://open.6api.net/mpic/s11284102.jpg",
          images_large: "http://open.6api.net/lpic/s11284102.jpg",
          isbn10: "7544258971",
          isbn13: "9787544258975",
          title: "霍乱时期的爱情",
          summary:
            "《霍乱时期的爱情》是加西亚•马尔克斯获得诺贝尔文学奖之后完成的第一部小说。讲述了一段跨越半个多世纪的爱情史诗，穷尽了所有爱情的可能性：忠贞的、隐秘的、粗暴的、羞怯的、柏拉图式的、放荡的、转瞬即逝的、生死相依的……再现了时光的无情流逝，被誉为“人类有史以来最伟大的爱情小说”，是20世纪最重要的经典文学巨著之一。",
          recommendByMe: false,
          onSale: false
        },
        {
          author: " 加西亚·马尔克斯",
          images_medium: "http://open.6api.net/mpic/s11284102.jpg",
          images_large: "http://open.6api.net/lpic/s11284102.jpg",
          isbn10: "7544258971",
          isbn13: "9787544258975",
          title: "霍乱时期的爱情",
          summary:
            "《霍乱时期的爱情》是加西亚•马尔克斯获得诺贝尔文学奖之后完成的第一部小说。讲述了一段跨越半个多世纪的爱情史诗，穷尽了所有爱情的可能性：忠贞的、隐秘的、粗暴的、羞怯的、柏拉图式的、放荡的、转瞬即逝的、生死相依的……再现了时光的无情流逝，被誉为“人类有史以来最伟大的爱情小说”，是20世纪最重要的经典文学巨著之一。",
          recommendByMe: true,
          onSale: false
        },
        {
          author: " 加西亚·马尔克斯",
          images_medium: "http://open.6api.net/mpic/s11284102.jpg",
          images_large: "http://open.6api.net/lpic/s11284102.jpg",
          isbn10: "7544258971",
          isbn13: "9787544258975",
          title: "霍乱时期的爱情霍乱时期的爱情",
          summary:
            "《霍乱时期的爱情》是加西亚•马尔克斯获得诺贝尔文学奖之后完成的第一部小说。讲述了一段跨越半个多世纪的爱情史诗，穷尽了所有爱情的可能性：忠贞的、隐秘的、粗暴的、羞怯的、柏拉图式的、放荡的、转瞬即逝的、生死相依的……再现了时光的无情流逝，被誉为“人类有史以来最伟大的爱情小说”，是20世纪最重要的经典文学巨著之一。",
          recommendByMe: false,
          onSale: true
        },
        {
          author: " 加西亚·马尔克斯",
          images_medium: "http://open.6api.net/mpic/s11284102.jpg",
          images_large: "http://open.6api.net/lpic/s11284102.jpg",
          isbn10: "7544258971",
          isbn13: "9787544258975",
          title: "霍乱时期的爱情",
          summary:
            "《霍乱时期的爱情》是加西亚•马尔克斯获得诺贝尔文学奖之后完成的第一部小说。讲述了一段跨越半个多世纪的爱情史诗，穷尽了所有爱情的可能性：忠贞的、隐秘的、粗暴的、羞怯的、柏拉图式的、放荡的、转瞬即逝的、生死相依的……再现了时光的无情流逝，被誉为“人类有史以来最伟大的爱情小说”，是20世纪最重要的经典文学巨著之一。",
          recommendByMe: true,
          onSale: true
        }
      ]
    }
  },
  methods: {
    navbarChange(e) {
      if(e === 0) {
        mpvue.redirectTo({
          url: '../books/main'
        })
      }
    },
    navigateToDetail() {
      mpvue.navigateTo({
          url: '../detail/main'
      })
    },
    navigateToRecommend() {
      mpvue.navigateTo({
          url: '../recommend/main'
      })
    },
    showModal() {
      mpvue.showModal({
        title: '还没写~~~'
      })
    }
  },
  components: {
    navBar
  }
}
</script>

<style lang="stylus" scoped>
@import './mine.styl'
</style>