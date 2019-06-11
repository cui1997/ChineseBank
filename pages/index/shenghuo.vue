<template>
	<view class="content">
<!-- 		<view class="top">
			<view class="location"><uni-icon type="location" size="30"></uni-icon></view>
			<view class="input"><input type="text" placeholder="农银快e付"></view>
			<view class="ting"><image src="../../static/img/jianting.png" style="width: 60upx;height: 60upx;"></image></view>
			<view class="xin"><uni-icon type="email" size="30"></uni-icon></view>
		</view> -->
		<view class="gg">
			<uni-grid :options='options' 
			:show-border="false"
				column-num="4">
			</uni-grid>
		</view>
		<view class="dddd">
			<!-- 滑块 -->
			<swiper :autoplay="true" :interval='2000' :circular='true' class="ggg">
				<swiper-item>
					<view><image style="height: 300upx;" src="../../static/img/t1.png" mode=""></image></view>
				</swiper-item>
				<swiper-item>
					<view><image style="height: 300upx;" src="../../static/img/t2.png" mode=""></image></view>
				</swiper-item>
				<swiper-item>
					<view><image style="height: 300upx;" src="../../static/img/t3.png" mode=""></image></view>
				</swiper-item>
			</swiper>
		</view>
		<view class="type">
			<view class="left">
				<view>贵金属商城</view>
				<view style="color: red;">诸事如意</view>
				<view><image src="../../static/img/t4.png" mode=""></image></view>
			</view>
			<view class="middle">
				<view>智慧食堂</view>
				<view style="color: red;">美食让你看见</view>
				<view><image src="../../static/img/t5.png" mode=""></image></view>
			</view>
			<view class="right">
				<view>个人中心</view>
				<view style="color: red;">订单详情</view>
				<view><image src="../../static/img/t6.png" mode=""></image></view>
			</view>
		</view>
		<view class="line"></view>
		<view class="youxiang">
			<view class="nav1">优享生活</view>
			<view class="nav2">></view>
		</view>
		<view class="t7">
			<image src="../../static/img/t7.png" mode=""></image>
		</view>
		<view class="type2">
			<view class="left">
				<view><image src="../../static/img/t8.png" mode=""></image></view>
				<view>华为P30系列</view>
				<view style="color: red;">火热销售中</view>			
			</view>
			<view class="middle">
				<view><image src="../../static/img/t9.png" mode=""></image></view>
				<view>vivoZ3手机</view>
				<view style="color: red;">6期0手续费</view>		
			</view>
			<view class="right">
				<view><image src="../../static/img/t10.png" mode=""></image></view>
				<view>OPPO Reno</view>
				<view style="color: red;">12期0手续费</view>
			</view>
		</view>
		<view class="pinzhi">
			<view class="nav1">品质商城</view>
			<view class="nav2">></view>
		</view>
		<view class="shop">
			<view class="l">
				<view class="t11"><image src="../../static/img/t11.png" mode=""></image></view>
			</view>
			<view class="r">
					<view class="t12">
						<view>积分优惠</view>
						<view style="color: red;">好物不花钱</view>
						<view><image src="../../static/img/t12.png" mode=""></image></view>
					</view>
					<view class="t13">
						<view><image src="../../static/img/t13.png" mode=""></image></view>
					</view>
					<view class="t14">
						<view>房产</view>
						<view style="color: red;">房多多专属房源</view>
						<view><image src="../../static/img/t14.png" mode=""></image></view>
					</view>
					<view class="t15">
						<view>大玩家</view>
						<view style="color: red;">挑战最强大脑</view>
						<view><image src="../../static/img/t15.png" mode=""></image></view>
					</view>	
		</view>
		</view>
					<view class="line"></view>
					<view class="fuwu">服务精选</view>
					<view class="down">
						<view class="t20"><image src="../../static/img/t20.png" mode=""></image></view>
						<view class="t21"><image src="../../static/img/t21.png" mode=""></image></view>
					</view>
					<view class="t100">
						<image src="../../static/img/jingdong.png" mode=""></image>
					</view>
		</view>
	
		
		
	</view>
</template>

<script>
	import uniGrid from "@dcloudio/uni-ui/lib/uni-grid/uni-grid.vue"
	import uniIcon from "@dcloudio/uni-ui/lib/uni-icon/uni-icon.vue"
	export default {
		components: {uniGrid,uniIcon},	
		data() {
			return {
				  options:[
					{image :'../../static/img/imgs/lifecost.png',text:'生活缴费'},
					{image:'../../static/img/imgs/money.png',text:'充值中心'},
					{image:'../../static/img/imgs/trip.png',text:'出行'},
					{image:'../../static/img/imgs/bean.jpg',text:'小豆'},
					{image:'../../static/img/imgs/location.jpg',text:'本地优惠'},
					{image:'../../static/img/imgs/yingpiao.jpg',text:'影票'},
					{image:'../../static/img/imgs/shopping.png',text:'商城'},
					{image:'../../static/img/imgs/all.png',text:'全部'}
					],
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.dddd{
		margin-top: 18upx;
	}
	.ggg{
		
		height: 300upx;
		margin-left: 43upx;
	}
	.gg{
		width: 100%;
	}
	.content {
		
		height: 400upx;
	}

	.logo {
		height: 200upx;
		width: 200upx;
		margin-top: 200upx;
	}

	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
	.input{
		width: 500upx;
		border: 1upx solid #000000;
		margin: 3px auto;
		border-radius:25px;	
		float: left;
	}
	.top{
		width: 100%;height: 50px;
		}
	.location{
		float: left;
	}
	.ting{
		float: left;	
	}
	.xin{
		float: right;
		margin-top: -2px;margin-right: 10px;
	}
	.type{
		margin-left:35upx;
		margin-top: 15upx;
	}
	.type .left,.type .middle,.type .right{
		display: inline-block;
		width: 190upx;
		font-size: 30upx;
		font-weight: bold;
		color: black;
		margin-left: 30upx;
		margin-top: 10upx;
	}
	.type image{
		width: 160upx;
		height: 130upx;
	}
	
	.type2{
		/* margin-left:35upx; */
		text-align: center;
		margin-top: 20upx;
	}
	.type2 .left,.type2 .middle,.type2 .right{
		display: inline-block;
		width: 200upx;
		font-size: 30upx;
		font-weight: bold;
		color: black;
		margin-left: 35upx;
	}
	.type2 image{
		width: 150upx;
		height: 130upx;
	}
	
	.line{
		background-color: #f4f4f4;
		width: 100%;
		height: 50upx;
	}
	.youxiang{
		margin-left: 40upx;
		margin-top: 40upx;
	}
	.pinzhi{
		margin-left: 40upx;
		margin-top: 75upx;
	}
	.nav1{
		font-weight: bold;
		margin-top: 20upx;
		}
	.nav2{
		font-size: 60upx;
		color: grey;
		float: right;
		margin-top: -70upx;
		}
		.t7 image{
		width: 100%;
		height: 300upx;
		}
		.shop{
			margin: 0 auto;
			margin-top: 30upx;
			height: 420upx;
		}
		.l{
			float: left;		
			width: 300upx;
			height: 390upx;
		}
		.t11 image{
			width: 300upx;
			height: 390upx;
			margin-left: 20upx;
		}
		.r{
			float: right;
			/* border: 1upx solid #000000; */
			width: 430upx;
			height:350upx;
			font-size: 30upx;
			text-align: center;
		}
		.t12,.t13,.t14,.t15{
			/* border: 1upx solid #0062CC; */
			width: 190upx;
			height: 170upx;
			float: left;
			margin-left: 20upx;
		}
		.t12 image{
			width: 100upx;
			height: 100upx;
		}
		.t13 image{
			width: 120upx;
			height: 180upx;
		}
		.t14 image,.t15 image{
			width: 100upx;
			height: 100upx;
		}
		.fuwu{
			margin-left: 40upx;
			margin-top: 40upx;
			font-weight: bold;
		}
		.down{
			margin-top: 20upx;
			/* height: 100upx; */
		}
		.t20 image,.t21 image{
			width: 320upx;
			height: 160upx;
			float: left;
			margin-left: 38upx;
		}
		.t100{
			
			margin-top: 50upx;
			height: 250upx;
		}
		.t100 image{
			margin-left: 40upx;
			margin-top: 35upx;
			  width: 680upx;
			  height: 200upx;
		}
	
</style>
