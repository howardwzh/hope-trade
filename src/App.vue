<template>
  <div id="app">
    <nav-menu :route-path="routePath"></nav-menu>
    <img src="./assets/logo.png">
    <router-view></router-view>
  </div>
</template>

<script>
import NavMenu from '@/components/NavMenu'

export default {
  name: 'app',
  created () {
    this.$data.routePath = this.$route.path
  },
  data () {
    return {
      routePath: ''
    }
  },
  components: {
    NavMenu
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
