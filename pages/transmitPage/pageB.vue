<template>
	<view class="content">
		<view class="titles">
			<view>A页面传过来的id:</view>
			<view class="contBox">{{content}}</view>
		</view>
		<!-- 小风车 -->
		<view class="xiaofc">
			<view class="fan">
				<div class="top"></div>
				<div class="right"></div>
				<div class="bottom"></div>
				<div class="left"></div>
			</view>
			<view class="stick"></view>
			<view class="dot"></view>
		</view>
		<view class="jiazaidh" @click="goJiazai()">加载动画</view>
		<view class="sdxcdai" @click="goxzPic()">小动画</view>
		<view class="sdxcdai" @click="gowyyPlay()">网易云</view>
		<view class="sdxcdai" @click="goTabs()">tab切换效果</view>
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
			// 跳转加载动画
			goJiazai(){
				uni.navigateTo({
					url:"/pages/min-animation/mni-loading/jz-loading"
				})
			},
			goxzPic(){
				uni.navigateTo({
					url:"/pages/min-animation/rotate-Pic/rotateImg"
				})
			},
			gowyyPlay(){
				uni.navigateTo({
					url:"/pages/min-animation/wyyMusic/wyy-playcover"
				})
			},
			goTabs(){
				console.log('1111');
				uni.navigateTo({
					url:"/pages/transmitPage/tabSwitch"
				})
			},
		}
	}
</script>

<style>
	@import url("pageB.css");
</style>