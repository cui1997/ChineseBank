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
.content {
	width: 90%;
	text-align: center;
	height: 700upx;
	margin: 0 auto;
}
.xtopimg{
	height: 360upx;
	width: 100%upx;
}
.xtopimg image{
	height: 100%;
	width: 100%;
}
.xtopimg button{
	background-color: aqua;
	width: 200upx;
	height: 60upx;
	z-index: 5;
	position: absolute;
	top: 250upx;
	left: 280upx;
}
.suo{
	position: absolute;
	left: 330upx;
	top: 110upx;
}
.v1{
	width: 100%;
	height: 320upx;
	background-color: #f4f4f4;
	padding: 1upx;
}
.v1-v1{
	width: 90%;
	height: 260upx;
	padding: 1upx;
	margin:30upx auto;
	background-color: white;
}
.v1-v1-h1{
	margin-top: 30upx;
	margin-left: 20upx;
}
.v1-v1-h2{
	position: absolute;
	left: 290upx;
	top: 850upx;
	color: red;
}
.v1-v1 p{
	font-size: 25upx;
	color: #ADADAD;
	position: absolute;
	top: 820upx;
	left: 330upx;
}
.v1-v1 button{
	background-color: aqua;
	width: 400upx;
	height: 60upx;
	z-index: 5;
	position: absolute;
	top: 910upx;
	left: 180upx;
}
.v2{
	height: 180upx;
	width: 100%;
}
.v2 image{
	width: 120upx;
	height: 120upx;
	margin-left: 30upx;
}
.v2-p1{
	font-size: 30upx;
	margin-left: 45upx;
}
.v2-p2{
	font-size: 30upx;
	margin-top: -120upx;
	margin-left: 250upx;
	margin-bottom: 20upx;
}
.v2-s1{
	color: red;
}
.v2-s2{
	margin-left: 310upx;
	font-size: 30upx;
}
.v2 button{
	color: aqua;
	width: 200upx;
	height: 60upx;
	margin-left: 540upx;
	font-size: 30upx;
	position: relative;
	top: -70upx;
}
.v3{
	height: 15upx;
	width: 100%;
	background-color: #F4F4F4;
}
.v4{
	height: 80upx;
	width: 90%;
	margin: 0 auto;
}
.v4 h1{
	margin-top: 45upx;
}
.v5{
	height: 640upx;
	width: 90%;
	margin: 0 auto;

}
.v5-v1 image{
	width: 100%;
	height: 250upx;
}
.v5-v2-v1{
	display: inline-block;
	height: 250upx;
	width: 222upx;

}
.v5-v2-v1 view{
	height: 100upx;
	width: 150upx;
	margin: 40upx auto;
}
.v5-v2-v1 image{
	height: 100upx;
	width: 150upx;
}
	
</style>
