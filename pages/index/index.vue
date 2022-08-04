<template>
	<view class="content">
		<image class="logo" src="/static/logo.png"></image>
		<view class="text-area">
			<text class="title">Welcome to vue</text>	
		</view>
		<button type="primary" @click="ILoveYou()">朱哥点一下</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {
			ILoveYou(){
				alert('博维是我的');
				alert('我看你是不服');
				alert('不服就来战');
				alert('立刻顺着网线过来打我');
				alert('怂了？');
				alert('这就不敢了？');
				alert('真不行啊');
				alert('就这就这？');
				alert('点那么快干嘛，点那么快博维就是我的');
				alert('你再点那么快？');
				alert('不要再点了');
				alert('能不能认真写代码');
				alert('不要在那里点alert框浪费时间');
				alert('赶紧干活');
				alert('别说我没提醒你');
				alert('我其实话很少,最爱干的事是一个人发呆。这样枯燥的我,真的会被大家喜欢吗?我很疑惑。如果你们能一层一层剥开我的内心,你们会发现,那颗心里写满了一句话:今天肯德基疯狂星期四,谁请我吃?');
				alert('我都懂，我都明白，我是选项E，我是planB，是分叉的头发，洗衣机流出的泡沫，超市里被捏碎的饼干，是吃腻的奶油，是落寞的城市，是地上的草，我是被踩踏的，是西装的备用扣，是被雨淋湿的小狗，是腐烂的橘子，是过期的牛奶，是断线的风筝，是被随意丢弃的向日葵，是沉默寡言的小朋友，所以能v我52吗，今天肯德基疯狂星期四。');
				alert('今天，是我人生中最黑暗、最emo的时候，但是我很难把朋友当成垃圾桶或者树洞去倾诉，更喜欢憋着自己消化，睡一觉第二天醒来就好了，不想连累别人，不想把负面情绪传递给身边的朋友。但是，我更希望家人能够给予我物质层面的帮助！今天是肯德基疯狂星期四，有哪个家人愿意请我吃肯德基吗?');			
				alert('我跟我男友相识快五年，这五年聚少离多，见他一面难如登天，喜欢他的人多如猪毛，长期没有安全感使我的内心非常痛苦。他约我今天七点半在tf直播间见面，我打算跟他彻底说清楚。说着我打开手机看时间，上面显示：肯德基疯狂星期四，热辣香骨鸡6块9块9，家人们，请我吃，增加我面对他时的勇气。');
				
			}

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
</style>
