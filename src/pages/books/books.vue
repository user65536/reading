<template>
  <div class="wrapper-books">
    <div class="top-nav">
      <div @click="topbarChange(0)" class="nav-item" :class="activeNavIndex === 0 ? 'active' : ''">已上架</div>
      <div @click="topbarChange(1)" class="nav-item" :class="activeNavIndex === 1 ? 'active' : ''">未上架</div>
    </div>
    <div class="content">
      <div class="books-wrap">
        <div v-for="(book, index) in books" :key="index" class="book-item">
          <div class="cover">
            <img class="img" :src="book.images_medium" alt>
          </div>
          <div class="title">{{book.title}}</div>
        </div>
      </div>
    </div>
    <nav-bar @navbarChange="navbarChange" :activeIndex="0"></nav-bar>
  </div>
</template>

<script>
import navBar from "@/components/navBar";
export default {
  data() {
    return {
      activeNavIndex: 0,
      books: [
        {
          levelNum: "8.0",
          subtitle: "",
          author: " 加西亚·马尔克斯",
          pubdate: "2012-9-1",
          origin_title: "El amor en los tiempos del cólera",
          binding: "精装",
          pages: "401",
          images_medium: "http://open.6api.net/mpic/s11284102.jpg",
          images_large: "http://open.6api.net/lpic/s11284102.jpg",
          publisher: "南海出版公司",
          isbn10: "7544258971",
          isbn13: "9787544258975",
          title: "霍乱时期的爱情",
          summary:
            "《霍乱时期的爱情》是加西亚•马尔克斯获得诺贝尔文学奖之后完成的第一部小说。讲述了一段跨越半个多世纪的爱情史诗，穷尽了所有爱情的可能性：忠贞的、隐秘的、粗暴的、羞怯的、柏拉图式的、放荡的、转瞬即逝的、生死相依的……再现了时光的无情流逝，被誉为“人类有史以来最伟大的爱情小说”，是20世纪最重要的经典文学巨著之一。",
          price: "39.50元"
        },
        {
          levelNum: "8.0",
          subtitle: "",
          author: " 加西亚·马尔克斯",
          pubdate: "2012-9-1",
          origin_title: "El amor en los tiempos del cólera",
          binding: "精装",
          pages: "401",
          images_medium: "http://open.6api.net/mpic/s11284102.jpg",
          images_large: "http://open.6api.net/lpic/s11284102.jpg",
          publisher: "南海出版公司",
          isbn10: "7544258971",
          isbn13: "9787544258975",
          title: "霍乱时期的爱情",
          summary:
            "《霍乱时期的爱情》是加西亚•马尔克斯获得诺贝尔文学奖之后完成的第一部小说。讲述了一段跨越半个多世纪的爱情史诗，穷尽了所有爱情的可能性：忠贞的、隐秘的、粗暴的、羞怯的、柏拉图式的、放荡的、转瞬即逝的、生死相依的……再现了时光的无情流逝，被誉为“人类有史以来最伟大的爱情小说”，是20世纪最重要的经典文学巨著之一。",
          price: "39.50元"
        },
        {
          levelNum: "8.0",
          subtitle: "",
          author: " 加西亚·马尔克斯",
          pubdate: "2012-9-1",
          origin_title: "El amor en los tiempos del cólera",
          binding: "精装",
          pages: "401",
          images_medium: "http://open.6api.net/mpic/s11284102.jpg",
          images_large: "http://open.6api.net/lpic/s11284102.jpg",
          publisher: "南海出版公司",
          isbn10: "7544258971",
          isbn13: "9787544258975",
          title: "霍乱时期的爱情",
          summary:
            "《霍乱时期的爱情》是加西亚•马尔克斯获得诺贝尔文学奖之后完成的第一部小说。讲述了一段跨越半个多世纪的爱情史诗，穷尽了所有爱情的可能性：忠贞的、隐秘的、粗暴的、羞怯的、柏拉图式的、放荡的、转瞬即逝的、生死相依的……再现了时光的无情流逝，被誉为“人类有史以来最伟大的爱情小说”，是20世纪最重要的经典文学巨著之一。",
          price: "39.50元"
        },
        {
          levelNum: "8.0",
          subtitle: "",
          author: " 加西亚·马尔克斯",
          pubdate: "2012-9-1",
          origin_title: "El amor en los tiempos del cólera",
          binding: "精装",
          pages: "401",
          images_medium: "http://open.6api.net/mpic/s11284102.jpg",
          images_large: "http://open.6api.net/lpic/s11284102.jpg",
          publisher: "南海出版公司",
          isbn10: "7544258971",
          isbn13: "9787544258975",
          title: "霍乱时期的爱情",
          summary:
            "《霍乱时期的爱情》是加西亚•马尔克斯获得诺贝尔文学奖之后完成的第一部小说。讲述了一段跨越半个多世纪的爱情史诗，穷尽了所有爱情的可能性：忠贞的、隐秘的、粗暴的、羞怯的、柏拉图式的、放荡的、转瞬即逝的、生死相依的……再现了时光的无情流逝，被誉为“人类有史以来最伟大的爱情小说”，是20世纪最重要的经典文学巨著之一。",
          price: "39.50元"
        },
        {
          levelNum: "8.0",
          subtitle: "",
          author: " 加西亚·马尔克斯",
          pubdate: "2012-9-1",
          origin_title: "El amor en los tiempos del cólera",
          binding: "精装",
          pages: "401",
          images_medium: "http://open.6api.net/mpic/s11284102.jpg",
          images_large: "http://open.6api.net/lpic/s11284102.jpg",
          publisher: "南海出版公司",
          isbn10: "7544258971",
          isbn13: "9787544258975",
          title: "霍乱时期的爱情霍乱时期的爱情",
          summary:
            "《霍乱时期的爱情》是加西亚•马尔克斯获得诺贝尔文学奖之后完成的第一部小说。讲述了一段跨越半个多世纪的爱情史诗，穷尽了所有爱情的可能性：忠贞的、隐秘的、粗暴的、羞怯的、柏拉图式的、放荡的、转瞬即逝的、生死相依的……再现了时光的无情流逝，被誉为“人类有史以来最伟大的爱情小说”，是20世纪最重要的经典文学巨著之一。",
          price: "39.50元"
        },
      ]
    };
  },
  methods: {
    navbarChange(e) {
      console.log(e)
    },
    topbarChange(index) {
      this.activeNavIndex = index
    }
  },
  components: {
    navBar
  }
};
</script>

<style lang="stylus" scoped>
@import './books.styl'
</style>