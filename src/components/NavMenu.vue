<template>
  <div class="nav-menu">
    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" @select="handleSelect">
      <el-menu-item index="1"><router-link to="/">首页</router-link></el-menu-item>
      <el-menu-item index="2"><router-link to="/list">产品列表</router-link></el-menu-item>
      <el-menu-item index="3"><router-link to="/about">关于我们</router-link></el-menu-item>
      <el-menu-item index="4"><router-link to="/contact">联系方式</router-link></el-menu-item>
    </el-menu>
  </div>
</template>

<script>
export default {
  name: 'nav-menu',
  created () {
    switch (this.routePath) {
      case '/':
        this.$data.activeIndex = '1'
        break
      case '/list':
        this.$data.activeIndex = '2'
        break
      case '/about':
        this.$data.activeIndex = '3'
        break
      case '/contact':
        this.$data.activeIndex = '4'
        break
    }
  },
  props: [
    'routePath'
  ],
  data () {
    return {
      activeIndex: '1'
    }
  },
  methods: {
    handleSelect (key) {
      console.log(key)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
