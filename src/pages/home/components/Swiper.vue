<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" />
            </swiper-slide>
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: '//img1.qunarzz.com/vc/a4/29/dd/4a0734b77f675da2a8ca4a9879.jpg'
      }, {
        id: '0002',
        imgUrl: '//img1.qunarzz.com/vc/30/e6/6c/7236d07f50947d523bcdeadae8.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
        background #fff
    .wrapper
        overflow hidden
        width 100%
        height 0
        padding-bottom 31.25%
        background #eee
        .swiper-img
            width 100%
</style>
