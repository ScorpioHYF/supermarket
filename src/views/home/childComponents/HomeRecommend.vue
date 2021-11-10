<template>
	<div class="recommends">
		<div v-for="(item, index) in recommendList" :key="index">
			<a :href="item.link">
				<img v-lazy="item.image">
				<p>{{item.title}}</p>
			</a>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'Recommend',
		props: {
			recommendList: {
				type: Array,
				default () {
					return []
				}
			}
		}
	}
</script>

<style scoped lang="less">
	.recommends {
		display: flex;
		text-align: center;
		font-size: 13px;
		padding: 15px 0 30px;
		border-bottom: 5px solid #eeeeee;

		&>div {
			flex: 1;
		}

		&>div img {
			width: 65px;
			height: 65px;
			margin-bottom: 5px;
		}
	}
</style>
