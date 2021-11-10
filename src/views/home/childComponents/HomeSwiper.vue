<template>
	<van-swipe :autoplay="3000">
		<van-swipe-item v-for="(item, index) in bannerList" :key="index">
			<a :href="item.link"><img v-lazy="item.image" /></a>
		</van-swipe-item>
	</van-swipe>
</template>

<script>
	export default {
		name: 'HomeSwiper',
		props: {
			bannerList: {
				type: Array,
				default () {
					return []
				}
			}
		}
	}
</script>

<style scoped lang="less">
	.van-swipe-item {
		img {
			max-width: 100%;
		}
	}
</style>
