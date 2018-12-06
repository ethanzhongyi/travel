<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class='content'>
      <detail-list :list='list'></detail-list>
    </div>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      list: [{
        title: '成人票',
        children: [{
          title: '成人票111',
          children: [{title: '成人票00000'}]
        },{
          title: '成人票222'
        }]
      },{
        title: '学生票',
        children: [{
          title: '学生票3333'
        },{
          title: '学生票4444'
        }]
      },{
        title: '儿童票',
        children: [{
          title: '儿童票555'
        },{
          title: '儿童票666'
        }]
      },{
        title: '特价票',
        children: [{
          title: '特价票777'
        },{
          title: '特价票888'
        }]
      }]
    }
  }
}
</script>

<style lang='stylus' scoped>
  .content
    height: 20rem
</style>
