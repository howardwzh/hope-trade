<template>
  <header class="header">
    <nav-menu></nav-menu>
  </header>
</template>

<script>
import NavMenu from '@/components/NavMenu'

export default {
  name: 'header',
  data () {
    return {
    }
  },
  components: {
    NavMenu
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>

</style>
