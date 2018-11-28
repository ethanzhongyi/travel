<template>
  <div class='icons'>
  <swiper>
    <swiper-slide v-for='(page, index) of pages' :key='index'
    >
      <div 
        class='icon' 
        v-for='item of page' 
        :key='item.id'
        >
        <div class='icon-img'>
          <img  class='icon-content' :src='item.imgUrl' />
        </div>
        <p class='icon-desc'>{{item.desc}}</p>
      </div>
    </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
    iconList: [{
    id: '0001',
    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
    desc: '热门景点热门景点'
    },{
    id: '0002',
    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
    desc: '深圳必游'
    },{
    id: '0003',
    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/8246f27355943202.png',
    desc: '游乐场'
    },{
    id: '0004',
    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
    desc: '文化古迹'
    },{
    id: '0005',
    imgUrl: 'https://img1.qunarzz.com/piao/fusion/1811/1d/c46140e32fffa502.png',
    desc: '去哪臻选'
    },{
    id: '0006',
    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png',
    desc: '野生动物园'
    },{
    id: '0007',
    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
    desc: '泡温泉'
    },{
    id: '0008',
    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
    desc: '一日游'
    },{
    id: '0009',
    imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
    desc: '一日'
    }]
    }
  },
  computed: {
  pages:function () {
    const pages = []
    this.iconList.forEach(function(item, index){
      const page = Math.floor(index / 8);
      if (!pages[page]) {
        pages[page] = [];
      }
      pages[page].push(item);
    })
    return pages;
  }
  }
}
</script>

<style lang='stylus' scoped>
  @import '~styles/varibles.styl'
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icon
    position: relative
    overfloat: hidden
    float:left
    width: 25%
    height: 0
    padding-bottom: 25%
    .icon-img
      position: absolute
      top: 0
      left: 0
      right: 0
      bottom: .44rem
      box-sizing: border-box
      padding: .1rem
      .icon-content
        display: block
        margin: 0 auto
        height: 100%
    .icon-desc
      position: absolute
      left: 0
      right: 0
      bottom: 0
      height: .44rem
      line-height: .44rem
      text-align: center
      color: $darktextColor
      overflow: hidden
      white-space: nowrap
      text-overflow: ellipsis
</style>