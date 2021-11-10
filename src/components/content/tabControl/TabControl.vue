<template>
	<div class="tab-control">
		<div class="tab-ctrl-item" v-for="(item, index) in titles" :key="index"
			:class="{active: index === currentIndex}" @click="itemClick(index)">
			<span>{{item}}</span>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'TabControl',
		props: {
			titles: {
				type: Array,
				default () {
					return []
				}
			}
		},
		data() {
			return {
				currentIndex: 0
			}
		},
		methods: {
			itemClick(index) {
				this.currentIndex = index
			}
		}
	}
</script>

<style scoped lang="less">
	.tab-control {
		display: flex;
		margin-top: 10px;
		height: 40px;
		line-height: 40px;
		text-align: center;

		.tab-ctrl-item {
			flex: 1;
		}

		.active {
			color: var(--color-high-text);

			span {
				border-bottom: 3px solid var(--color-tint);
				padding: 5px;
			}
		}
	}
</style>
