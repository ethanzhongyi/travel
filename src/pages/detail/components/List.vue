<template>
  <div>
    <div
      class='item'
      v-for='(item, index) of list'
      :ker='index'
    >
  	  <div class='item-title'>
  	    <span class='item-title-icon border-bottom'></span>
  	    {{item.title}}
  	  </div>
  	  <div v-if='item.children' class='item-children'>
  	    <detail-list :list='item.children'></detail-list>
  	  </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>

<style lang='stylus' scoped>
  @import '~styles/varibles.styl'
  .item-title-icon
    display: inline-block;
    position: relative;
    width: .36rem;
    height: .36rem;
    top: .05rem;
    left: .1rem;
    background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat;
    margin-right: .2rem;
    background-size: .4rem 3rem;
  .item-title
    line-height: .8rem
    font-size: .32rem
    padding: 0 .2rem
  .item-children
    padding: 0 .2rem
    
  
</style>
