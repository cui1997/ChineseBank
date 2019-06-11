<template>
	<view class="content">
	<!-- 	<view><uni-icon type="scan" size="20"></uni-icon><mSearch @search="search($event,0)"></mSearch>
        {{val0}}<br/>
		</view>	 -->	
		<view>
			<wuc-tab :tab-list="tabList" :tabCur.sync="TabCur" @change="tabChange" textFlex='true'></wuc-tab>
			<view v-if="TabCur==0">
			<unigridA></unigridA>
			</view>
			<view v-else="TabCur==1">
			<unigridB></unigridB>
			</view>
			</view>
	<image class="nyzt" src="../../static/img/nyzt.JPG"></image>
	<view id="hqinvestor">
	<h3>活期投资</h3>
	<view class="investor">
		<image class="images"  src="../../static/invest/nykeb.jpg"></image><span class="investor-spa">农银快e宝</span></br>
		<span class="investor-span">货币基金</span><span class="investor-span">1分起投</span>
		<span class="investor-spana">2.48%</span></br>
		<span class="investor-spanb">七日年化收益率</span>
		</view>
	<view class="investor">
		<image class="images" src="../../static/invest/ssf.jpg"></image><span class="investor-spa">时时付</span></br>
		<span class="investor-span">开放式理财</span><span class="investor-span">申赎灵活</span>
		<span class="investor-spana">3.44%</span></br>
		<span class="investor-spanb">七日年化收益率</span>
	      </view>
	    </view>
	<view  class="Invest-regularly">
		<h3>定期投资</h3>
		<view class="regularly-Investa">
		<span class="investor-span">"本利丰·360天"人民</span></br>
		<span class="investor-span">币理财产品</span></br>
		<span class="investor-spana">3.65%</span></br>
		<span class="investor-spanb">360天</span>
		</view>
		<view class="regularly-Investb">
			<span class="investor-span">"金钥匙·汇利丰"2019</span></br>
			<span class="investor-span">年第293期人民币结构...</span></br>
			<span class="investor-spana">3.55%-3.65%</span></br>
			<span class="investor-spanb">365天</span></view>
		<!-- <view class="regularly-Invest">
			<span class="investor-span">"安心·每年安放"第九</span></br>
			<span class="investor-span">期人民币理财产品...</span></br>
			<span class="investor-spana">4.2%</span></br>
			<span class="investor-spanb">最低持有360天</span></view>
		</view> -->
	</view>
	<view class="Optimizing-fund">
		<h3>优选基金</h3>
		<view class="fund-OptimizingA">
			<p><span class="investor-spanaa">2.01%</span>
			<span class="investor-spanab">富国宏观策略</span></p>		
			<p><span class="investor-spanba">季涨幅</span>
			<span class="investor-spanbb">000029</span></p>
		</view>
		<view class="fund-Optimizing">
			<p><span class="investor-spanaa">3.58%</span>
			<span class="investor-spanab">华安黄金联接A类</span></p>		
			<p><span class="investor-spanba">月涨幅</span>
			<span class="investor-spanbb">000216</span></p>
		</view>
	</view>
	<image class="nyzt" src="../../static/invest/tzjyzq.JPG"></image>
	<view id="Maxmessage">
		<h3>资讯</h3><uni-icon type="arrowright" size="24"></uni-icon>
		<view class="messageA">
			<span class="message-span">
			<span class="investor-spanbc">中国农业银行基金投研动态</span></br>
			<span class="investor-spanbc">(2019.5.20-5.26)</span></br>
			<span class="investor-spanbd">市场要闻|2019-05-28</span></span>
			<image class="message-imgA" src="../../static/invest/lhc.JPG"></image>
			<hr>
		</view>
		<view class="messageB">
			<span class="message-span">
			<span class="investor-spanbc">谦晟鸿:美元依旧强势黄金上行乏</span></br>
			<span class="investor-spanbc">力下周看冲高回落</span></br>
			<span class="investor-spanbd">专家视点|2019-05-2</span></span>
			<image class="message-imgB" src="../../static/invest/qsp.JPG"></image>
		</view>
	</view>
	</view>
</template>

<script>
	import mSearch from '@/components/mehaotian-search/mehaotian-search.vue'
	import uniIcon from "@/components/uni-icon/uni-icon.vue"
	import WucTab from '@/components/wuc-tab/wuc-tab.vue'
	import unigridA from '../invest/unigridA.vue'
	import unigridB from '../invest/unigridB.vue'
	export default {
		 components: {WucTab,mSearch,uniIcon,unigridA,unigridB},
		data() {
			return {
				 val0: '',
				  placeholder:'农银快e付',
				  TabCur: 0,
				  tabList: [{ name: '业务1' }, { name: '业务2' }],
			}
		},
		onLoad() {

		},
		methods: {
            search(e, val) {
            console.log(e, val);
            this['val'+val] = e;
         },
		 tabChange(index) {
		 		this.TabCur = index;
		 	}
		 }
		}
</script>

<style>
	page{
		background-color:#EEF2EF ;
	}
	wuc-tab{
		background-color:#FFFFFF;
	}
	.nyzt{
	margin-top:15upx;
	width:750upx;
	height:200upx;
	}
	#hqinvestor{
	width:750upx;
	height:340upx;
	background-color:#FFFFFF;
	}
	h3{
		padding-top:35upx;
		margin-left:30upx;
	}
	.investor{
		text-align: center;
		background-color:#FEFFFF;
		margin:10upx 20upx 0upx 20upx;
		padding-left:36upx;
		display:inline-block;
		height:220upx;
		width:300upx;
		margin-left:10upx;
	}
	.investor-span{
		font-size:30upx;
		margin-left:12upx;
	}
	.investor-spana{
		color:#ECC681;
		font-size:46upx;
		padding-top:30upx;
	}
	.investor-spanb{	
		font-size:22upx;
		font-weight:200;
	}
	.images{
		width:30upx;
		height:30upx;
	}
	.Invest-regularly{
		margin-top:30upx;
		width:750upx;
		height:300upx;
		background-color:#FFFFFF;
	}
	.investor-spa{
		font-size:35supx;
		}
	.regularly-Investa{
		display:inline-block;
		text-align: center;
		margin-left:20upx;
		width: 350upx;
		height:220upx;
		border-right:1px solid;
	}
    .regularly-Investb{
		display:inline-block;
		text-align: center;
		margin-left:20upx;
		width: 350upx;
		height:220upx;
	}
	.Optimizing-fund{
		margin-top:20upx;
		width:750upx;
		height:360upx;
		background-color:#FFFFFF;
	}
	.fund-OptimizingA{
		padding-top:15upx;
		width:750upx;
		height:130upx;
		border-bottom:1px solid;
	}
	.fund-Optimizing{
		width:750upx;
		height:160upx;
	}
	.investor-spanaa{
		color:#ECC681;
		font-size:46upx;
		padding:40upx 0upx 0upx 30upx;
	}
	.investor-spanab{
		font-size:30upx;
		margin-left:120upx;
		}
	.investor-spanba{
		font-size:22upx;
		font-weight:300;
		padding:30upx 0upx 0upx 30upx;
		}
		
	.investor-spanbb{
		font-size:22upx;
		font-weight:300;
		margin-left:180upx;
	}
	#Maxmessage{
		margin-top:20upx;
		width:750upx;
		height:700upx;
		background-color:#FFFFFF;
	}
	uni-icon{
		 position: absolute;
		 left:700upx;
		 margin-top:-45upx;
	}
	.investor-spanbc{
		font-size:30upx;
		margin-left:40upx;
		padding-top:30upx;
	}
	.investor-spanbd{
		font-size:22upx;
		font-weight:300;
		margin-left:40upx;
		padding-top:10upx;
	}
	.message-span{
		margin-top:50upx;
	}
	.messageA{
        padding-top:30upx ;
		height:280upx;
		width:750upx;
	}
	.messageB{
		padding-top:30upx;
		height:280upx;
		width:750upx;
	}
	.message-imgA{
		width:270upx;
		height:240upx;
		margin-top:-140upx;
        padding-left:470upx;
	}
	.message-imgB{
		width:270upx;
		height:240upx;
		margin-top:-140upx;
	    padding-left:470upx;
	}
</style>
