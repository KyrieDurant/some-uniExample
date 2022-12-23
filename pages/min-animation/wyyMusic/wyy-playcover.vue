<template>
	<view class="content">
		<!-- 背景图片 -->
		<view class="bgVague">
			<image style="width: 100%; height: 100%; filter: blur(20rpx);background-size: cover;"
				src="../../../static/image/xzPic/winter-four.jpg" mode=""></image>
		</view>
		<!-- 页面内容 -->
		<view class="pageCont">
			<!-- 页面上方内容 -->
			<view class="pageTop">
				<view class="">Music Name</view>
				<view class="">作者：</view>
			</view>
			<!-- 页面中间部分 -->
			<view class="pageCenter">
				<!-- 放大线 -->
				<view class="enlargeLine1"></view>
				<view class="enlargeLine2"></view>
				<view class="enlargeLine3"></view>
				<!-- 圆盘 -->
				<view class="platform">
					<image src="../../../static/image/xzPic/winter-one.jpg" mode="aspectFit"
						style="width: 100%; height: 100%;"></image>
				</view>

			</view>
			<!-- 页面底部 -->
			<view class="PageBottom">
				<!-- 上面小图标 -->
				<view class="smxtb">
					<view class="smxtb1" v-for="(item,index) in tbList" :key="index">
						<view class="smxtbPic" @click="goBut(item.funct)">
							<image :src="item.img" mode="aspectFit" style="width: 100%; height: 100%;"></image>
						</view>
					</view>
				</view>
				<!-- 中间滑动选择器 -->
				<view class="playhd">
					<!-- 开始时间 -->
					<view class="kstime">00:00</view>
					<!-- 进度条 -->
					<view class="jdtime">
						<slider @change="sliderChange()" min="0" max="100"
						block-size="10" activeColor="#8bb8ff"/>
					</view>
					<!-- 结尾时间 -->
					<view class="jstime">7:11</view>
				</view>
				<!-- 下面操作键 -->
				<view class="xmBtn">
					<!-- 心动模式 -->
					<view class="xm-item">
						<view class="xmanPic">
							<image src="../../../static/image/wyy/xdms.png"
							 mode="aspectFit" style="width: 100%; height: 100%;"></image>
						</view>
					</view>
					<!-- 上一曲 -->
					<view class="xm-item">
						<view class="xmanPic">
							<image src="../../../static/image/wyy/syq.png"
							 mode="aspectFit" style="width: 100%; height: 100%;"></image>
						</view>
					</view>
					<!-- 暂停/播放 -->
					<view class="xm-item2">
						<view class="xmanPic2">
							<image src="../../../static/image/wyy/bf.png"
							 mode="aspectFit" style="width: 100%; height: 100%;"></image>
						</view>
					</view>
					<!-- 下一曲 -->
					<view class="xm-item">
						<view class="xmanPic">
							<image src="../../../static/image/wyy/xyq.png"
							 mode="aspectFit" style="width: 100%; height: 100%;"></image>
						</view>
					</view>
					<!-- 音乐列表 -->
					<view class="xm-item">
						<view class="xmanPic">
							<image src="../../../static/image/wyy/yylb.png"
							 mode="aspectFit" style="width: 100%; height: 100%;"></image>
						</view>
					</view>
				</view>
			</view>
		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				tbList: [{
						img: '../../../static/image/wyy/axwd.png',
						funct: 1,
					},
					{
						img: '../../../static/image/wyy/xz.png',
						funct: 2,
					},
					{
						img: '../../../static/image/wyy/ld.png',
						funct: 3,
					},
					{
						img: '../../../static/image/wyy/pl.png',
						funct: 4,
					},
					{
						img: '../../../static/image/wyy/gd.png',
						funct: 5,
					},
				]
			}
		},
		onLoad() {

		},
		methods: {
			goBut(row) {
				if (row == 1) {
					this.likeit();
				} else if (row == 2) {
					this.mudownLoad();
				}
			},
			likeit() {
				console.log('点击爱心');
			},
			mudownLoad() {
				console.log('点击下载音乐');
			},

			sliderChange(e) {
				console.log('value 发生变化：' + e.detail.value)
			},

		},
	}
</script>

<style>
	@import url("wyy-playcover.css");
</style>
