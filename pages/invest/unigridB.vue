<template>
		<view class="content">
			<uni-grid :options="[
			    {image:'../../static/invest/jsh.jpg',text:'结售汇'},
			    {image:'../../static/invest/zsb.jpg',text:'债市宝'},
			    {image:'../../static/invest/bx.jpg',text:'保险'},
			    {image:'../../static/invest/yzzz.jpg',text:'银证转账'},
			    {image:'../../static/invest/yqzz.jpg',text:'银期转账'},
			    {image:'../../static/invest/jsq.jpg',text:'计算器'},
			    {image:'../../static/invest/ll.jpg',text:'利率'},
			    {image:'../../static/invest/shjf.jpg',text:'生活缴费'}]" 
			    column-num="4" :show-border="false" type="square"  >
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
.content{
	background-color:#FFFFFF;
}
</style>


