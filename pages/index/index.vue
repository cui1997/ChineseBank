<template>
	<view class="content">
			
		  <swiper class="swiper" :indicator-dots="false" :autoplay="true" :interval="2000" :duration="duration">
                        <swiper-item>
                            <view class="swiper-item uni-bg-red"><image src="../../static/img/dong.jpg" mode=""></image></view>
                        </swiper-item>
                        <swiper-item>
                            <view class="swiper-item uni-bg-green"><image src="../../static/img/zhong.jpg" mode=""></image></view>
                        </swiper-item>
                        <swiper-item>
                            <view class="swiper-item uni-bg-blue"><image src="../../static/img/dong1.jpg" mode=""></image></view>
                        </swiper-item>
          </swiper>


	<view id="qq">下午好 !</view>
    <view>
		<uni-grid :options="options" :show-border="false" column-num="4">
		</uni-grid>
    </view>
	 <view id="da">
	         <view class="aa">金融小蜜书 千事万事都靠ta</view>    
			 <view class="dd1"> <view @click="nf" type="warn" style=" text-align: center; width: 90upx; height: 90upx; border-radius:50%; color:white;background:#6AE3E4; line-height: 80upx;">GO</view>
			 </view> 
			 <view id="daa">
			 <view class="vv"><image src="../../static/img/@PVSL4QB158DE9%5B6S$M%7BPJN.png"></image>缴费提醒</view>
			 <view class="vv"><image src="../../static/img/GKNE53NF3%7DTQVEU8~J1ZG5K.png"></image>还款提醒</view>
			 <view class="vv"><image src="../../static/img/SUF400ZZ137GT)SHD8[{2BQ.png"></image>个人提醒</view>
			 </view>
	 </view>	
	 <view id="ff"><image src="../../static/img/zhong.jpg"></image></view>
     <view class="hh">存款专区</view>
     <view id="gg">
     	<view class="xx"><image src="../../static/img/gg1.jpg"></image></view>
     	<view class="xx"><image src="../../static/img/gg2.jpg"></image></view>
        <view class="xx"><image src="../../static/img/gg3.jpg"></image></view>
     </view>
	 <view class="hhh">为您推荐</view>
	  <view id="hhhh">
        <uni-segmented-control :current="current" :values="items" @clickItem="onClickItem" style-type="text" active-color="#EF6C2E"></uni-segmented-control>
        <view class="pl">
            <view v-show="current === 0" class="ccc">
		    <view class="vvv">全球限量限时秒杀:</view>
			  <uni-countdown
				color="#333131"
				background-color="#EFA5A5" 
				border-color="#EFA5A5" 
				:day="1" 
				:hour="2" 
				:minute="30" 
				:second="0">
			   </uni-countdown>
            </view>
            <view v-show="current === 1">
            <hh></hh>
            </view>
            <view v-show="current === 2">
                此处是会员用户请先登陆验证
				<login></login>
            </view>
        </view>
    </view>
	</view>
</template>

<script>
 
	import  uniCountdown from  '@dcloudio/uni-ui/lib/uni-countdown/uni-countdown.vue'
	import hh from "../indexs/hh.vue"
	import login from "../indexs/login.vue"
	import tupian from "../indexs/tupian.vue"
	import uniSegmentedControl from '@dcloudio/uni-ui/lib/uni-segmented-control/uni-segmented-control.vue'
	import uniGrid from '@dcloudio/uni-ui/lib/uni-grid/uni-grid.vue'
	export default {
	components: {uniGrid,uniSegmentedControl,uniCountdown,hh,login,tupian},
		data() {

			return {
			options:[
					 {image:'../../static/img/user.jpg',text:'我的账户', value:0},
				     {image:'../../static/img/user3.jpg',text:'转帐', value:1},
			         {image:'../../static/img/user4.jpg',text:'理财', value:2},
					 {image:'../../static/img/user7.jpg',text:'贷款', value:3},
					 {image:'../../static/img/user5.jpg',text:'充值中心', value:4},
					 {image:'../../static/img/user2.jpg',text:'保险', value:5},
					 {image:'../../static/img/user8.png',text:'基金', value:6},
					 {image:'../../static/img/user6.png',text:'全部', value:7},
			],
				
	        items: ['日常专区','活动专区','会员专区'],
            current: 0,
			index:0
			}
		},
		onLoad() {

		},
		methods: {
           onClickItem(index) {
            if (this.current !== index) {
                this.current = index;
            } 
        }
/* 		fn(options){
			if (options.index==7){
				uni.navigateTo({
					url: '../indexs/register?id='+options.index
				})
			}
			
		} */

		}
	}
</script>

<style>
	.xx image{
		width: 230upx;
		height: 130upx;
		float: left;
		margin-left: 20upx;
		margin-top: 26upx;
		
	}
	.hh{
		margin-top: 30upx;
	    margin-right: 540upx;
	}
	.hhh{
		margin-top: 180upx;
	    margin-right: 540upx;
	}
	#hhhh{
		margin-top: 20upx;
		margin-left: -100upx;
	}
	.vvv{
		color:#EFA5A5;
		margin-left: -130upx;
		margin-top: 10upx;
		font-style: oblique;
		font-size: 50upx;
	}
	.ccc{
		width:-10upx;
		height: 40upx;
	}
	#qq{

		font-size: 55upx;
       margin-left: -500upx;
	   margin-top: 30upx;
		color:#10AC33;

	}
	.content {
		text-align: center;
		height: 400upx;
	}
	.pl {
		text-align: center;
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
	.swiper image{
		width: 100%;
		height: 420upx;
	}
		.swiper{
		width: 100%;
		height: 390upx;
	    margin-top: 1upx;
	}
	.content{
		width: 100%;
	}
	
	 #da{
		width: 100%;
		height: 250upx;
		margin-top: 25upx;
	}
	    #daa{
			padding-left: -50upx;
		width: 100%;
		height: 200upx;
		margin-top: -50upx;
	
	}
	.dd1{
		margin-left: 580upx;
		margin-top: -20upx;

	}
	.vv{
		float: left;
		margin-left: 10upx;
		font-size: 28upx;
		color: #AAA4A4;
	}
    .vv image{
    	width: 60upx;
    	height: 50upx;
    	
    }
	.aa{
	font-style: oblique;
		color: #897E7E;
		margin-left: -235upx;
	}
		#ff{
	width: 100%;
	height: 210upx;
	margin-top: -60upx;
	
	}
	#ff image{
		width: 100%;
		height: 210upx;
	
	}
</style>

