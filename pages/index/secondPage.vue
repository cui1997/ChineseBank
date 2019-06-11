<template>
    <view class="head">
        <view class="header-wrap">
            <view class="index-header">
                <text class="address" v-if="leftWords">{{leftWords}}</text>
                <view class="input-wrap" v-if="input">
                    <input type="text" 
                           placeholder="请输入搜索"
                            v-model="value"
                           @change="inputChange"/>
                    <text class="iconfont iconfangdajing"></text>
                </view>
                <view class="map-wrap"
                      v-if="rightWords||rightIcon"
                      @click="rightClick">
                    <text class="iconfont" :class="rightIcon"></text>
                    <text>{{rightWords}}</text>
                </view>
            </view>
        </view>
        <view class="blank"></view>

    </view>
</template>

<script>
    export default {
        name: "IndexHeader",
        props: [
            'leftWords',
            'input',
            'rightIcon',
            'rightWords'
        ],
        data () {
            return {
                value: ''
            }
        },
        methods: {
            inputChange: function () {
                this.$emit('change',this.value)
            },
            rightClick: function () {
                this.$emit("rightClick")
            }
        }
    }
</script>

<style lang="scss">
    $color-base: #00c16f; 
    $words-color-base: #333333;
    $words-color-light: #999999; 
    .header-wrap {
        width: 100%;
        position: fixed;
        top: 0;
        z-index: 999;
        
        .index-header {
            height: 88upx;
            line-height: 88upx;
            padding: 0 30upx;
            padding-top: 40upx;
            background-color: $color-base;
            font-size: 28upx;
            color: #fff;
            display: flex;
            align-items: center;
            justify-content: space-between;
            
            .address {
                font-size: 26upx;
            }
            
            .input-wrap {
                width: 500upx;
                height: 70upx;
                padding: 10upx 30upx 10upx 100upx;
                box-sizing: border-box;
                background-color: #fff;
                border-radius: 50upx;
                color: $words-color-base;
                position: relative;
                
                text {
                    position: absolute;
                    left: 40upx;
                    top: -8upx;
                    color: $words-color-light;
                    font-size: 30upx;
                }
            }
            
            .map-wrap {
                .iconfont {
                    font-size: 32upx;
                    margin-right: 5upx;
                }
                text {
                    font-size: 26upx;
                }
            }    
        }
    }
    .blank {
        height: 126upx;
    }
</style>
