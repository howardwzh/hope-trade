<template>
  <div id="app">
    <page-header></page-header>
    <div class="page-body">
      <router-view></router-view>
    </div>
    <page-footer></page-footer>
  </div>
</template>

<script>
import PageHeader from '@/components/Header'
import PageFooter from '@/components/Footer'

export default {
  name: 'app',
  data () {
    return {
    }
  },
  components: {
    PageHeader,
    PageFooter
  }
}
</script>

<style lang="less">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  .page-body {
    min-height: 500px;
  }
}
</style>
