<template>
  <div class="home">
    <carousel-banner></carousel-banner>
	<div>
		<div class="group-header clearfix">
			<h3 class="group-title">新品</h3>
			<a class="look-more" href="#">查看更多>></a>
		</div>
		<cards-group></cards-group>
	</div>
	<div>
		<div class="group-header clearfix">
			<h3 class="group-title">热门</h3>
			<a class="look-more" href="#">查看更多>></a>
		</div>
		<cards-group></cards-group>
	</div>
	<div>
		<div class="group-header clearfix">
			<h3 class="group-title">特色</h3>
			<a class="look-more" href="#">查看更多>></a>
		</div>
		<cards-group></cards-group>
	</div>
  </div>
</template>

<script>
import CarouselBanner from '@/components/CarouselBanner'
import CardsGroup from '@/components/CardsGroup'

export default {
  name: 'home',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components: {
    CarouselBanner,
    CardsGroup
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
.group-header {
	padding: 0 12px;
	text-align: right;
	line-height: 40px;
	.group-title {
		float: left;
		margin: 0;
	}
}
</style>
