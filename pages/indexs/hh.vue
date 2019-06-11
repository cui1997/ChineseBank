<template>
	<view class="content">

		<view>
         <view class="uni-padding-wrap uni-common-mt">
            <view>
                <video id="myVideo" src="https://dcloud-img.oss-cn-hangzhou.aliyuncs.com/guide/uniapp/%E7%AC%AC1%E8%AE%B2%EF%BC%88uni-app%E4%BA%A7%E5%93%81%E4%BB%8B%E7%BB%8D%EF%BC%89-%20DCloud%E5%AE%98%E6%96%B9%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B@20181126.mp4"
                    @error="videoErrorCallback" :danmu-list="true"  enable-danmu danmu-btn controls></video>
            </view>

            <view class="uni-list uni-common-mt">
                <view class="uni-list-cell">
                    <view>
                        <view class="uni-label"></view>
                    </view>
                    <view class="uni-list-cell-db">
                        <input v-model="danmuValue" class="uni-input" type="text" placeholder="在此处输入弹幕内容" />
                    </view>
                </view>
            </view>
            <view class="uni-btn-v">
                <button @click="sendDanmu" class="page-body-button" type="primary">发送弹幕</button>
            </view>

        </view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				 src: '',
            danmuList: [{
                    text: '第 1s 出现的弹幕',
                    color: '#ff0000',
                    time: 1
                },
                {
                    text: '第 3s 出现的弹幕',
                    color: '#ff00ff',
                    time: 3
                }
            ],
            danmuValue: ''
		
			}
		},
	    onReady: function(res) {
     
        this.videoContext = uni.createVideoContext('myVideo')
  
        },
		methods: {
             sendDanmu: function() {
            this.videoContext.sendDanmu({
                text: this.danmuValue,
                color: this.getRandomColor()
            });
            this.danmuValue = '';
        },
        videoErrorCallback: function(e) {
            uni.showModal({
                content: e.target.errMsg,
                showCancel: false
            })
        },
        getRandomColor: function() {
            const rgb = []
            for (let i = 0; i < 3; ++i) {
                let color = Math.floor(Math.random() * 256).toString(16)
                color = color.length == 1 ? '0' + color : color
                rgb.push(color)
            }
            return '#' + rgb.join('')
        }
		}
	}
</script>

<style>
	.content {
		text-align: center;
		height: 700upx;
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
	video{
		width: 600upx;
		height: 400upx;
		margin-top: 60upx;
		margin-left: 50upx;
	}
	.page-body-button{
		width: 250upx;
		height: 80upx;
		font-size: 25upx;
	}
	.uni-input{
	font-size: 50upx;
	margin-top: 30upx;

	}
	.page-body-button{
	margin-top: 30upx;
	}
</style>

