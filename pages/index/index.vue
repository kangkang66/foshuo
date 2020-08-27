<template>
	<view class="wrap">
		<u-swiper :list="list" :title="true"></u-swiper>
		
		<view class="cu-list grid col-3 no-border" >
			<view class="cu-item" v-for="(item,index) in cuIconList" :key="index" >
				<view :class="['cuIcon-' + item.cuIcon,'text-' + item.color]">
					<view class="cu-tag badge" v-if="item.badge!=0">
						<block v-if="item.badge!=1">{{item.badge>99?'99+':item.badge}}</block>
					</view>
				</view>
				<text>{{item.name}}</text>
			</view>
		</view>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list: [{
						image: 'https://cdn.uviewui.com/uview/swiper/1.jpg',
						title: '昨夜星辰昨夜风，画楼西畔桂堂东'
					},
					{
						image: 'https://cdn.uviewui.com/uview/swiper/2.jpg',
						title: '身无彩凤双飞翼，心有灵犀一点通'
					},
					{
						image: 'https://cdn.uviewui.com/uview/swiper/3.jpg',
						title: '谁念西风独自凉，萧萧黄叶闭疏窗，沉思往事立残阳'
					}
				],
				cuIconList: [{
					cuIcon: 'cardboardfill',
					color: 'red',
					badge: 120,
					name: '忏悔'
				}, {
					cuIcon: 'recordfill',
					color: 'orange',
					badge: 1,
					name: '视频'
				}, {
					cuIcon: 'picfill',
					color: 'yellow',
					badge: 0,
					name: '佛图'
				}, {
					cuIcon: 'noticefill',
					color: 'olive',
					badge: 22,
					name: '通知'
				}, {
					cuIcon: 'commandfill',
					color: 'purple',
					badge: 0,
					name: '交流'
				}, {
					cuIcon: 'discoverfill',
					color: 'purple',
					badge: 0,
					name: '探索'
				}],
				gridCol: 3,
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss" scoped>
	.wrap {
		padding: 40rpx;
	}
</style>