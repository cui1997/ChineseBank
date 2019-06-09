<template>
	<view>
		<view class="content">
			<!-- 头部图片 -->
			<view class="xtopimg">
				<image src="../../static/xinyongka/yinghangka.jpg"></image>
				<uni-icon type="locked" size="50" class="suo" color="white"></uni-icon>
				<button size="mini">点击登录</button>
			</view>
			<!-- 头部小图标 -->
			<uni-grid :options="arr"
				column-num="4"
				:show-border="false">
			</uni-grid>
		</view>
		<!-- 备用金 -->
		<view class="v1">
			<view class="v1-v1">
				<h1 class="v1-v1-h1">备用金</h1>
				<p>最高额度</p>
				<h1 class="v1-v1-h2">300,000元</h1>
				<button size="mini">立即进入</button>
			</view>
		</view>
		<view class="v2">
			<image src="../../static/xinyongka/9.jpg"></image>
			<p class="v2-p1">信用币</p>
			<p class="v2-p2">最高<span class="v2-s1">20,000</span>秒速到账</p>
			<span class="v2-s2">小额信用贷</span>
			<button type="primary" plain="true" size="mini">点击进入</button>
		</view>
		<view class="v3"></view>
		<view class="v4">
			<h1>精品优惠</h1>
		</view>
		<view class="v5">
			<view class="v5-v1">
				<image src="../../static/ka2/1.png"></image>
			</view>
			<view class="v5-v2">
				<view class="v5-v2-v1">
					<view><image src="../../static/ka2/2.jpg"></image></view>
				</view>
				<view class="v5-v2-v1">
					<view><image src="../../static/ka2/3.jpg"></image></view>
				</view>
				<view class="v5-v2-v1">
					<view><image src="../../static/ka2/4.jpg"></image></view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	import uniGrid from '@dcloudio/uni-ui/lib/uni-grid/uni-grid.vue'
	import uniIcon from "@dcloudio/uni-ui/lib/uni-icon/uni-icon.vue"
	export default {
		components: {uniGrid,uniIcon},
		data() {
			return {
				arr:[{image:"../../static/xinyongka/1.png",text:"我要还款"},
				{image:"../../static/xinyongka/2.jpg",text:"现金分期"},
				{image:"../../static/xinyongka/3.jpg",text:"现金转出"},
				{image:"../../static/xinyongka/4.png",text:"额度调整"},
				{image:"../../static/xinyongka/5.png",text:"我要办卡"},
				{image:"../../static/xinyongka/6.jpg",text:"进度查询"},
				{image:"../../static/xinyongka/7.png",text:"积分权益"},
				{image:"../../static/xinyongka/8.jpg",text:"设置"},
				]
			}
		},
		onLoad() {

		},
		methods: {
			
		}
	}
</script>

<style>
	@import url("../../static/css/xinyongka");
	
</style>
