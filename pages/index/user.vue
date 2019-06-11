<template>
	<view class="center">
		<view class="logo" @click="goLogin" :hover-class="!login ? 'logo-hover' : ''">
			<image class="logo-img" :src="login ? uerInfo.avatarUrl :avatarUrl"></image>
			<view class="logo-title">
				<text class="uer-name">Hi，{{login ? uerInfo.name : '您未登录'}}</text>
				<text class="go-login navigat-arrow" v-if="!login">&#xe65e;</text>
			</view>
		</view>
		<view class="center-list">
			<view class="center-list-item border-bottom">
				<text class="list-text">我的资产</text>
				<text class="navigat-arrow">&#xe65e;</text>
					
			</view>
		<view class="dd">
		<view><image src="../../static/img1/11.png"></image></view>
		</view>
		</view>
			<view class="center-list1">
			<view class="center-list-item">
			<text class="list-text">我的生活</text>
			</view>
			<view class="type">
			<view class="left">
				<view><image src="../../static/img1/1.jpg"></image></view>
				<view class="list">积分</view>
			</view>
			<view class="middle">
				<view><image src="../../static/img1/2.jpg"></image></view>
				<view class="middle1">小豆</view>
			</view>
			<view class="right">
				<view><image src="../../static/img1/3.png"></image></view>
				<view class="reght1">礼券</view>
			</view>
			</view>
			
		</view>
		<view class="center-list2">
			<view class="center-list-item border-bottom" @click="fn">
				<text class="list-text">安全中心</text>
				<input type="text" v-model="telno" placeholder="保护您的账户安全!" disabled/>
				<text class="navigat-arrow" >&#xe65e;</text>
			</view>
			</view>
			<view class="center-list3">
				<view class="center-list-item border-bottom">
					<text class="list-text">网点服务</text>
				</view>
				<view class="pd">
					<view><image src="../../static/img1/4.jpg"></image></view>
					<view class="pd1">排队</view>
				</view>
				<view class="xc">
				<view><image src="../../static/img1/5.jpg"></image></view>
				<view class="xc1">现钞</view>
				</view>
				<view class="wb">
				<view><image src="../../static/img1/6.jpg"></image></view>
				<view class="wb1">外币</view>
				</view>
				<view class="jn">
				<view><image src="../../static/img1/7.jpg"></image></view>
				<view class="jn1">纪念币预约</view>
				</view>
				</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				login: false,
				avatarUrl: "../../static/img1/logo.png",
				uerInfo: {}
			}
		},
		methods: {
			goLogin() {
			uni.navigateTo({
			url:"../indexs/login"
		})
			},
			fn(){
				uni.navigateTo({
					url:"../index/user1"
				})
			}
		}
	}
</script>

<style>
	@import url("../../static/css/wdfw.css");
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

	page {
		background-color: #f8f8f8;
	}

	.center {
		flex-direction: column;
	}

	.logo {
		width: 750upx;
		height: 280upx;
		padding: 20upx;
		box-sizing: border-box;
		background-color: #575757;
		flex-direction: row;
		align-items: center;
	}

	.logo-hover {
		opacity: 0.8;
	}

	.logo-img {
		width: 150upx;
		height: 150upx;
		border-radius: 150upx;
	}

	.logo-title {
		height: 150upx;
		flex: 1;
		align-items: center;
		justify-content: space-between;
		flex-direction: row;
		margin-left: 20upx;
	}

	.uer-name {
		height: 60upx;
		line-height: 60upx;
		font-size: 38upx;
		color: #FFFFFF;
	}

	.go-login.navigat-arrow {
		font-size: 38upx;
		color: #FFFFFF;
	}

	.login-title {
		height: 150upx;
		align-items: self-start;
		justify-content: center;
		flex-direction: column;
		margin-left: 20upx;
	}

	.center-list {
		background-color: #FFFFFF;
		margin-top: 20upx;
		width: 750upx;
		height: 300upx;
		flex-direction: column;
	}

	.center-list-item {
		height: 90upx;
		width: 750upx;
		box-sizing: border-box;
		flex-direction: row;
		padding: 0upx 20upx;
		
	}

	.border-bottom {
		border-bottom-width: 1upx;
		border-color: #c8c7cc;
		
	}

	.list-icon {
		width: 40upx;
		height: 90upx;
		line-height: 90upx;
		font-size: 34upx;
		color: #4cd964;
		text-align: center;
		font-family: texticons;
		margin-right: 20upx;
		
	}

	.list-text {
		height: 90upx;
		line-height: 90upx;
		font-size: 35upx;
		color: #555;
		flex: 1;
		text-align: left;
		font-weight:bold;
		letter-spacing:8upx;
		
	}

	.navigat-arrow {
		height: 90upx;
		width: 40upx;
		line-height: 90upx;
		font-size: 34upx;
		color: #555;
		text-align: right;
		font-family: texticons;
	}
	.center-list1{
		background-color: #FFFFFF;
		margin-top: 20upx;
		width: 750upx;
		height: 200upx;
		flex-direction: column;
	}

	
		
</style>