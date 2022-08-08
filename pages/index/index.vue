<template>
	<view class="content">
		<!-- <image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">Welcome to vue</text>	
		</view> -->
		<!-- 选择按钮 -->
		<view class="button-area">
			<navigator url="../createList/createList" hover-class="button-hover">
				<view class="button creat-button">
					创建表单
				</view>
			</navigator>
			<navigator url="../finalList/finalList" hover-class="button-hover">
				<view class="button final-button"> 
					历史表单
				</view>
			</navigator>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				// title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
			
		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
		margin-bottom: 20px;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
	
	.button{
		width: 250rpx;
		height: 250rpx;
		margin-top: 300rpx;
		background-color: aliceblue;
		color: #6f9eeb;
		text-align: center;
		font-size: 40rpx;
		line-height: 250rpx;
		border-radius:8rpx;
		border: 1rpx solid #d6e2f6;
	}
	
	.final-button{
		margin-left:95rpx;
	}
	
	.button-area{
		display: flex;
		flex-direction: row;
		/* background-color: #6f9eeb; */
		width: 80%;
		
	}
</style>
