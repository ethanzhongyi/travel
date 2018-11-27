<template>
<div class='wrapper'>
  <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for='item of swiperList' v-bind:key='item.id'>
      <img class='swiper-img' :src='item.imgUrl' />
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/8c/b9e86352f9aa5f02.jpg_750x200_2fe2875f.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/4d/6706bf772c05ce02.jpg_750x200_773e75f0.jpg'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/61/44400d6591891202.jpg_750x200_7565a05c.jpg'
      }]
    }
  }
}
</script>

<style lang='stylus' scoped>
    .wrapper >>> .swiper-pagination-bullet-active
      background: #fff
    .swiper-img
      width: 100%

</style>
