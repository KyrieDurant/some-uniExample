<template>
	<view class="content">
		<view class="titles">
			<view>传过来的id:</view>
			<view class="contBox">{{content}}</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				content:'',
			}
		},
		onLoad(option) {
			console.log('我接收到', option);
			this.content = option.id;
			console.log('拿到id的值', this.content);
		},
		methods: {
	
		}
	}
</script>

<style>
	.content{
		display: flex;
		justify-content: center;
	}
	.titles{
		height: 100rpx;
		width: 100%;
		display: flex;
		justify-content: baseline;
		align-items: center;
	}
	
	.contBox{
		width: 100rpx;
		height: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
		color: #fff;
		margin-left: 10rpx;
		background-color: rgb(51, 51, 77);
	}
</style>