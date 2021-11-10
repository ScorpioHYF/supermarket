<template>
	<tab-bar>

		<tab-bar-item itemlink="/home">
			<img slot="item-icon" src="~assets/img/tabbar/icon01.png" alt="home">
			<img slot="item-icon-active" src="~assets/img/tabbar/icon01_active.png" alt="home">
			<div slot="item-text">首页</div>
		</tab-bar-item>

		<tab-bar-item itemlink="/category">
			<img slot="item-icon" src="~assets/img/tabbar/icon02.png" alt="categories">
			<img slot="item-icon-active" src="~assets/img/tabbar/icon02_active.png" alt="categories">
			<div slot="item-text">分类</div>
		</tab-bar-item>

		<tab-bar-item itemlink="/cart">
			<img slot="item-icon" src="~assets/img/tabbar/icon03.png" alt="shopcart">
			<img slot="item-icon-active" src="~assets/img/tabbar/icon03_active.png" alt="shopcart">
			<div slot="item-text">购物车</div>
		</tab-bar-item>

		<tab-bar-item itemlink="/profile">
			<img slot="item-icon" src="~assets/img/tabbar/icon04.png" alt="profile">
			<img slot="item-icon-active" src="~assets/img/tabbar/icon04_active.png" alt="profile">
			<div slot="item-text">我的</div>
		</tab-bar-item>

	</tab-bar>
</template>

<script>
	import TabBar from 'components/common/tabbar/TabBar'
	import TabBarItem from 'components/common/tabbar/TabBarItem'

	export default {
		name: "MainTabBar",
		data() {
			return {}
		},
		components: {
			TabBar,
			TabBarItem
		}
	}
</script>

<style scoped>

</style>
