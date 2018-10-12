<template>
  <div class="wrapper">
    <swiper :options="swiperOption" ref="mySwiper">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
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
        // 小圆点点击切换图片，轮播图下面的
        loop: true
        // 支持轮播
      },
      swiperList: [{
        id: '01',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1801/bd/04554e7c67650302.jpg_750x200_4293d60a.jpg'
      },
      {
        id: '02',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/82/c94c9a77de17f902.jpg_750x200_a8419488.jpg'
      }]
    }
  }
}
</script>

<style lang="scss" scoped>
  .wrapper /deep/ .swiper-pagination-bullet-active{
       background: #fff;
     }
  .wrapper{
    overflow: hidden;
    width:100%;
    height:0;
    padding-bottom:31.25%;
     .swiper-img{
       width:100%;
      }
  }
</style>
