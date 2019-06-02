<template>
  <div class="icons border-bottom">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
           <img class="icon-content" :src="item.iconUrl" alt="">
          </div>
          <p class="icon-desc">{{item.iconDesc}}</p>
        </div>
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>

</template>
<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  data  () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        paginationClickable: true
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';
.icons >>> .swiper-container
  margin-top 0.15rem
  overflow hidden
  height 0
  padding-bottom 49.33%
.icons >>> .swiper-pagination-bullet
  width 0.12rem
  height 0.12rem
.icons >>> .swiper-pagination-bullet-active
  background-color $bgColor
.icon
  position relative
  overflow hidden
  float left
  width 25%
  height 0
  padding-bottom 22%
  .icon-img
    overflow hidden
    position absolute
    top 0
    left 0
    right 0
    bottom 0.42rem
    box-sizing border-box
    padding 0.06rem
    .icon-content
      display block
      height  100%
      margin 0 auto
  .icon-desc
    position absolute
    left 0
    right 0
    bottom 0
    line-height 0.43rem
    height 0.43rem
    color $darkTextColor
    text-align center
    ellipsis()
</style>
