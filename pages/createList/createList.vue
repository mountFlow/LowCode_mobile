<template>
	<view>
	<!-- 新建图标 -->
	<view class="drawPaper">
		<view class="iconfont creat_icon">&#xe64b;</view>	
	</view>
	<!-- 功能折叠菜单栏 -->
	<!-- 使用了uni-collapse 折叠面板插件 -->
	<view class="functionMenu">
		<uni-collapse accordion>
	<!-- 选择组件 -->
			<uni-collapse-item title="组件" :open="true">
				<scroll-view scroll-top="scrollTop" scroll-y="true">
					<!-- 使用了uni-row 布局-行插件 -->
				<uni-row> 
					<uni-col :span="8" v-for="(item,index) in moduleInfoOne" :key="index">
						<view class="module_area">
							<view :class="'iconfont '+ item.mIcon +' module_icon'"></view>
							<view class="module_name">{{ item.mName }}</view>
						</view>
					</uni-col>
				</uni-row>
				</scroll-view>
			</uni-collapse-item>
	<!-- 编辑样式 -->
			<uni-collapse-item title="样式">
				<scroll-view class="style_area">
					<!-- 使用了uni-segmented-control 分段器插件 -->
				  <uni-segmented-control :current="current" :values="styleItems" @clickItem="onClickItem" styleType="text" activeColor="#0055ff"></uni-segmented-control>
				        <view class="content">
							
							<!-- 组件选择卡内容 -->
				            <view v-show="current === 0">
								<!-- 颜色选择器 使用了https://ext.dcloud.net.cn/plugin?id=403 -->
				                <button class="color_btn" type="primary" @click="showPickerColorPop()">点我选择组件颜色</button>
				            </view>
							
							<!-- 字体选择卡内容 -->
				            <view v-show="current === 1">
								<view class="text_style">
									<view class="text_size_text">大小</view>
									<slider class="text_size_slider" value="50" name="slider" show-value></slider>
								</view>
				                <button class="color_btn" type="primary" @click="showPickerColorPop()">点我选择文本颜色</button>
				            </view>
							
							<!-- 背景选择卡内容 -->
				            <view v-show="current === 2">
				                <button class="color_btn" type="primary" @click="showPickerColorPop()">点我选择背景颜色</button>
				            </view>
				        </view>	
                        
				</scroll-view>
			</uni-collapse-item>
			<!-- 确定发布 -->
			<uni-collapse-item title="确定发布" :open="true">
				<view class="submit_area">
					<navigator url="../submitList/submitList" hover-class="button-hover">
						<button class="submit_btn" type="primary">发布</button>
					</navigator>
				</view>
			</uni-collapse-item>
		</uni-collapse>
	</view>
	<picker-color :isShow="showPickerColor" :bottom="0"  @callback='getPickerColor' />
	</view>
</template>

<script>
	import pickerColor from "@/components/helang-pickerColor/helang-pickerColor.vue"
	export default {
		components: {
			"picker-color":pickerColor,
		},
		data() {
			return {
				// 组件数组(图标,名称)
				moduleInfoOne:[
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
					{
						mName : "单行文本框",
						mIcon : 'icon-textBox'
					},
					{
						mName : "日期选择器",
						mIcon : 'icon-riqixuanzeqi'
					},
					{
						mName : "单选",
						mIcon : 'icon-danxuan'
					}
				],
				// 样式分类
				styleItems: ['组件', '文本','背景'],
				current: 0,
				//组件样式颜色选择器
				buttonColor:"#0099FF",
				showPickerColor:false,
				bottomPickerColor:0
			}
		},
		methods: {
			// 分段器方法
			onClickItem(e) {
			      if (this.current != e.currentIndex) {
			        this.current = e.currentIndex;
			      }
			},
			// 显示获取颜色选择弹窗
			 showPickerColorPop(){
			    this.showPickerColor=true;
			},
			// 获取颜色选择回调
			getPickerColor(color){
			    /* 隐藏弹窗 */
			    this.showPickerColor = false;
			     /* 判断颜色值是否有效 */
			    if(color){
			        this.buttonColor = color;
			        console.log('选择的颜色值是：'+color);
			    }
			}
		}
	}
</script>

<style>
	page{
		background-color: #c9daf8;
	}
	/* 画布 */
	.drawPaper{
		width: 95%;
		height: 1000rpx;
		background-color: white;
		margin: 0 auto;
		box-shadow: 0rpx 0rpx 1rpx 1rpx #EAEFF3;
	}
	
	/* 折叠框 */
	.functionMenu{
		/* bottom: 0; */
		width: 100%;
		height: 200rpx;
		margin-bottom: 0rpx;
	}
	
	/* 组件图标 */
	.module_icon{
		font-size: 50rpx;
		text-align: center;
	}
	
	/* 组件栏 */
	.module_area{
		margin-bottom: 20rpx;
		/* margin-top: 20rpx; */
	}
	
	/* 组件名称 */
	.module_name{
		margin: 0 auto;
		text-align: center;
		padding-top: 10rpx;
	}
	
	/* 画布中的新建图标 */
	.creat_icon{
		font-size: 100rpx;
		text-align: center;
		padding-top: 300rpx;
	}
	
	/* 样式栏 */
	.style_area{
		margin-bottom: 20rpx;
		text-align: center;
		margin: 0 auto;
		height: 500rpx;
	}
	
	/* 字体选择卡 */
	.text_style{
		display: flex;
		flex-direction: row;
		width: 100%;
		padding-top: 20rpx;
		margin-top: 20rpx;
		margin-bottom: 20rpx;
	}
	
	.text_size_slider{
		width: 80%;
		padding-left: 0rpx;
	}
	
	.text_size_text{
		text-align: center;
		margin: 0 auto;
		font-size: 35rpx;
		margin-top: 10rpx;
	}
	
	.color_btn{
		width: 60%;
		margin-top: 50rpx;
	}
	
	/* 确定发布栏 */
	.submit_area{
		/* margin: 0 auto; */
		height: 300rpx;
	}
	
	.submit_btn{
		width: 60%;
		margin-top: 50rpx;
	}
</style>
