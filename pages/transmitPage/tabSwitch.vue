<template>
	<view class="content">
		<view class="tabBox">
			<view class="atabs" v-for="(item,index) in tabList" :key="index">
				<view @click="getTitle(index)" :class="clils == index ? 'aTab' : 'aTab2'">{{item.name}}</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data(){
			return {
				tabList:[
					{
						name: '标题1',
					},
					{
						name: '标题2',
					},
					{
						name: '标题3',
					},
					{
						name: '标题4',
					},
				],
				clils: 0,
			}
		},
		onLoad() {
			
		},
		methods:{
			getTitle(e){
				this.clils = e;
				console.log('得到',e);
			},
		},
	}
</script>

<style >
page{
	width:100%;
	height:100%;
}
.content{
	width:100%;
	height:100%;
	display:flex;
}
.tabBox{
	width: 100%;
	height: 100rpx;
	margin-top: 100rpx;
	background-color: #ccc;
	display: flex;
}
.atabs{
	height: 100%;
	width: 100%;
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: #3ab0bd;
}
.aTab{
	width: 100%;
	height: 100%;
	display: flex;
	justify-content: center;
	align-items: center;
	border: 1rpx solid #ccc;
	color: #fff;
	background-color: #65bd36;
}
.aTab2{
	width: 100%;
	height: 100%;
	display: flex;
	justify-content: center;
	align-items: center;
	border: 1rpx solid #ccc;
	color: #fff;
	background-color: #aaaaff;
}
</style>