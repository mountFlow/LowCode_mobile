<template>
	<view>
	<!-- 添加图标 -->
	<view class="drawPaper">
		<view class="iconfont creat_icon">&#xe64b;</view>	
	</view>
	<!-- 功能折叠菜单栏 -->
	<view class="functionMenu">
		<uni-collapse accordion>
	<!-- 选择组件 -->
			<uni-collapse-item title="组件" :open="true">
				<uni-table border stripe>
					<uni-tr>
						<uni-td class="module_area" v-for="(item,index) in moduleInfo" :key="item" :span="4">
							<!-- v-for="(mName,mIcon) in moduleInfo -->
							<view :class="'iconfont '+ item.mIcon +' module_icon'"></view>
							<view class="module_name">{{ item.mName }}</view>
						</uni-td>
					</uni-tr>
				</uni-table>	
			</uni-collapse-item>
	<!-- 编辑样式 -->
			<uni-collapse-item title="样式">I
				<text>h</text>	
			</uni-collapse-item>
		</uni-collapse>
	</view>
	
	</view>
</template>

<script>
	export default {
		data() {
			return {
				moduleInfo:[
					{
						mName : "按钮",
						mIcon : 'icon-anniu'
					},
					{
						mName : "多行文本框",
						mIcon : 'icon-fuwenbenkuang'
					},
					{
						mName : "多选",
						mIcon : 'icon-duoxuan'
					},
					
				]
					
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	page{
		background-color: #c9daf8;
	}
	
	.drawPaper{
		width: 95%;
		height: 1000rpx;
		background-color: white;
		margin: 0 auto;
		box-shadow: 0rpx 0rpx 1rpx 1rpx #EAEFF3;
	}
	
	.functionMenu{
		bottom: 0;
		width: 100%;
		height: 200rpx;
	}
	
	.module_icon{
		font-size: 50rpx;
		text-align: center;
	}
	
	.module_area{
		width: 30%;
		align: center;
		height: 200rpx;
		
	}
	
	.module_name{
		margin: 0 auto;
		text-align: center;
		padding-top: 10rpx;
	}
	
	.creat_icon{
		font-size: 100rpx;
		text-align: center;
		padding-top: 300rpx;
	}
</style>
