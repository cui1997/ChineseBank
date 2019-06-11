<template>
		<view class="center">
			<uni-grid :options="[
			    {image:'../../static/invest/lc.jpg',text:'理财'},
			    {image:'../../static/invest/ssf.jpg',text:'时时付'},
			    {image:'../../static/invest/jj.jpg',text:'基金'},
			    {image:'../../static/invest/nykeb.jpg',text:'农银快e宝'},
			    {image:'../../static/invest/nyzt.jpg',text:'农银智投'},
			    {image:'../../static/invest/ck.jpg',text:'存款'},
			    {image:'../../static/invest/zhgjs.jpg',text:'账户贵金属'},
			    {image:'../../static/invest/cjt.jpg',text:'存金通'}]" 
			    column-num="4" :show-border="false" type="square" >
				</uni-grid>
		</view>
</template>

<script>
	import uniGrid from "@/components/uni-grid/uni-grid.vue"
	export default {
		 components: {uniGrid},
		data() {
			return {
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
.center{
	background-color:#FFFFFF;
}
</style>

