<template>
	<view class="center">
		
		<view class="center-list">
		<view class="center-list-item border-bottom">
		<text class="list-text">密码管理</text>
			</view>
			<uni-grid :options="[
				{image:'../../static/imgs/1.png',text:'登录密码'},
				{image:'../../static/imgs/2.jpg',text:'手势密码'},
				{image:'../../static/imgs/3.jpg',text:'指纹/人脸'},
				{image:'../../static/imgs/4.jpg',text:'刷脸验证'}]" 
				:show-border="false"
				column-num="4">
			</uni-grid>
			</view>
			<view class="center-list">
			<view class="center-list-item border-bottom">
			<text class="list-text">支付管理</text>		
		</view>
			<uni-grid :options="[
				{image:'../../static/imgs/5.png',text:'快e付设置'},
				{image:'../../static/imgs/6.png',text:'快捷支付解约'},
				{image:'../../static/imgs/7.png',text:'账户管理'}]"
				:show-border="false"
				column-num="4">
			</uni-grid>		
		</view>	
		<view class="center-list">
			<view class="center-list-item border-bottom">
			<text class="list-text">介质管理</text>		
		</view>
			<uni-grid :options="[
				{image:'../../static/imgs/8.png',text:'切换安全工具'},
				{image:'../../static/imgs/9.png',text:'k宝设置'},
				{image:'../../static/imgs/10.png',text:'k令设置'}]"
				:show-border="false"
				column-num="4">
			</uni-grid>		
		</view>		
	</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue"

	export default {
		components: {uniGrid},
		
		data() {
			return {
				login: false,
				avatarUrl: "../../static/uni-center/logo.png",
				uerInfo: {}
			}
		},
		methods: {
			goLogin() {
				if (!this.login) {
					console.log("点击前往登录")
				}
			}
		}
	}
</script>

<style>
	@font-face {
		font-family: texticons;
		font-weight: normal;
		font-style: normal;
		src: url('https://at.alicdn.com/t/font_984210_5cs13ndgqsn.ttf') format('truetype');
	}

	page,
	view {
		display: flex;
	}

	

	.center {
		flex-direction: column;
		background-color: #F1F1F1;
	}

	.center-list {
		margin-top: 20upx;
		width: 750upx;
		height: 300upx;
		flex-direction: column;
		background-color: #FFFFFF;
	}

	.center-list-item {
		height: 90upx;
		width: 750upx;
		box-sizing: border-box;
		flex-direction: row;
		padding: 0upx 20upx;
		
	}

	

	.list-text {
		height: 90upx;
		line-height: 90upx;
		font-size: 35upx;
		color: #555;
		flex: 1;
		text-align: left;
		letter-spacing:8upx;
		
	}

</style>