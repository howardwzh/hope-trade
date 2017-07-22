<template>
  <div class="nav-menu">
    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
      <el-menu-item index="0">首页</el-menu-item>
      <el-menu-item index="1">产品列表</el-menu-item>
      <el-menu-item index="2">关于我们</el-menu-item>
      <el-menu-item index="3">联系方式</el-menu-item>
    </el-menu>
  </div>
</template>

<script>
import Router from 'vue-router'
import _ from 'lodash'
const router = new Router()
const pathArr = ['/', '/list', '/about', '/contact']

export default {
  name: 'nav-menu',
  created () {
    this.$data.activeIndex = _.toString(_.indexOf(pathArr, this.$route.path))
  },
  data () {
    return {
      activeIndex: '0'
    }
  },
  methods: {
    handleSelect (key) {
      router.push({
        path: pathArr[key]
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>

</style>
