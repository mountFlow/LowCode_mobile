<template>
	<view>
		<uni-row class="area photo_area" :gutter="gutter" :width="nvueWidth">
		<!-- 设置封面 -->
			
			<!-- 封面文本 -->
			<uni-col :span="5" :offset="2">
				<view class="title photo_title">封面</view>
			</uni-col>
			
			<!-- 封面图片 -->
			<uni-col class="photo" :span="3" :offset="1">
				<view>
					<image class="photo" mode="aspectFit" src="../../static/logo.png"></image>
				</view>
			</uni-col>
			
			<!-- 封面图标 -->
			<uni-col :span="3" :offset="10">
				<view class="iconfont icon-youjiantou photo_icon"></view>
			</uni-col>
			
		<!-- 分割线 -->
			<uni-col :span="22" :offset="1">
				<view class="divider"></view>
			</uni-col>
			
		<!-- 命名 -->
		
			<!-- 命名标题 -->
			<uni-col :span="4" :offset="2">
				<view class="title name_title">名字</view>
			</uni-col>
			
			<!-- 表单名字 -->
			<uni-col :span="12" :offset="2">
				<view class="text name_text">调查问卷</view>
			</uni-col>
			
			<!-- 命名图标 -->
			<uni-col :span="1" :offset="21">
				<view class="iconfont icon-youjiantou name_icon"></view>
			</uni-col>
			
		<!-- 分割线 -->
			<uni-col :span="22" :offset="1">
				<view class="divider"></view>
			</uni-col>	
			
		<!-- 表格开放时间 -->
		
			<!-- 标题 -->
			<uni-col :span="6" :offset="2">
				<view class="title time_title">开放时间</view>
			</uni-col>
			
			<!-- 时间选择器 -->
			<!-- 使用了uni-datetime-picker 日期选择器插件 -->
			<uni-col :span="20" :offset="2">
				<view class="datatime">
					<uni-datetime-picker v-model="datetimerange" type="datetimerange" rangeSeparator="至" />
				</view>
			</uni-col>
			
		<!-- 分割线 -->
			<uni-col :span="22" :offset="1">
				<view class="divider"></view>
			</uni-col>
			
		<!-- 是否每个用户只能答一次 -->
			
			<!-- 标题 -->
			<uni-col :span="13" :offset="2">
				<view class="title ">每个用户只能提交一次</view>
			</uni-col>
			
			<!-- switch按钮 -->
			<uni-col :span="2" :offset="17">
				<view class="uni-form-item uni-column">
					<switch name="switch" />
				</view>
			</uni-col>
			
		<!-- 分割线 -->
			<uni-col :span="22" :offset="1">
				<view class="divider"></view>
			</uni-col>
		
		<!-- 记录用户昵称 -->
		
			<!-- 标题 -->
			<uni-col :span="13" :offset="2">
				<view class="title ">记录用户昵称</view>
			</uni-col>
			
			<!-- switch按钮 -->
			<uni-col :span="2" :offset="17">
				<view class="uni-form-item uni-column">
					<switch name="switch" />
				</view>
			</uni-col>
		
		<!-- 分割线 -->
			<uni-col :span="22" :offset="1">
				<view class="divider"></view>
			</uni-col>
			
		<!-- 提交 -->
			<uni-col :span="8" :offset="8">
				<button type="primary" class="QRcode">提交</button>
			</uni-col>
		
		</uni-row>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.area{
		margin-top: 30rpx;
	}

	.title{
		font-size: 35rpx;
		text-align: left;
		margin-top: 20rpx;
	}

	.photo{
		height: 100rpx;
		border-radius: 5rpx;
	}

	.iconfont{
		font-size: 60rpx;
	}
	
	.photo_icon{
		margin-top: 15rpx;
	}
	
	.divider{
		height: 1rpx;
		background-color: #cad3dc;
		margin-top: 20rpx;
	}
	
	.text{
		color: #878787;
		margin-top: 20rpx;
		font-size: 35rpx;
		text-align: right;
	}
	
	.name_icon{
		margin-top: -50rpx;
	}
	
	.datatime{
		margin-top: 20rpx;
	}
	
	.uni-form-item{
		margin-top: -50rpx;
	}
	
	.QRcode{
		margin-top: 100rpx;
	}
</style>
