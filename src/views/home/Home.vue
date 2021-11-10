<template>
	<div id="home">
		<!-- 导航栏 -->
		<nav-bar class="home-nav">
			<div slot="center">购物街</div>
		</nav-bar>

		<!-- 轮播图 -->
		<home-swiper class="banner" :bannerList="banners.list" />

		<!-- 推荐信息 -->
		<home-recommend :recommendList="recommends.list" />

		<!-- 本周流行 -->
		<home-feature />

		<!-- 切断菜单 -->
		<tab-control :titles="['流行','新款','精选']" />

		<ul>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
			<li>asditemClickitemClickitemClick</li>
		</ul>

	</div>
</template>

<script>
	import NavBar from 'components/common/navbar/NavBar'
	import TabControl from 'components/content/tabControl/TabControl'

	import HomeSwiper from './childComponents/HomeSwiper'
	import HomeRecommend from './childComponents/HomeRecommend'
	import HomeFeature from './childComponents/HomeFeature'

	import {
		getMultidata
	} from 'network/home'

	export default {
		name: "Home",
		components: {
			NavBar,
			HomeSwiper,
			HomeRecommend,
			HomeFeature,
			TabControl
		},
		data() {
			return {
				banners: [],
				dKeywords: [],
				keywords: [],
				recommends: [],
				isLoading: false,
			}
		},
		created() {
			getMultidata().then(res => {
				this.banners = res.data.banner
				this.dKeywords = res.data.dKeyword
				this.keywords = res.data.keywords
				this.recommends = res.data.recommend
			})
		}
	}
</script>

<style scoped>
	#home {
		margin-bottom: 50px;
	}

	.home-nav {
		background-color: var(--color-tint);
		color: #fff;
		position: sticky;
		top: 0;
		left: 0;
		right: 0;
		z-index: 9;
	}

	.tab-control {
		position: sticky;
		top: 44px;
		background-color: #fff;
		z-index: 9;
	}
</style>
