<template>
	<view class="container">
		<view class="uni-padding-wrap">
			<view class="page-section swiper">
				<view class="page-section-spacing">
					<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
						<swiper-item><img src="../../static/1.png" /></swiper-item>
						<swiper-item><img src="../../static/2.png" /></swiper-item>
						<swiper-item><img src="../../static/2.png" /></swiper-item>
					</swiper>
				</view>
			</view>
		</view>

		<view class="userinfo">
			<text>{{name}}</text>
			<text>{{day}}</text>
		</view>

		<view class="showinfo">
			<p>Yesterday is history, </p>
			<p>tomorrow is a mystery, </p>
			<p>but today is a gift,</p>
			<p>That is why it is called the present</p>
		</view>

		<view class="menu">
			<uni-grid :column="3" :square="false">
				<uni-grid-item>
					Vue专题
				</uni-grid-item>
				<uni-grid-item>
					Vue专题
				</uni-grid-item>
				<uni-grid-item>
					Vue专题
				</uni-grid-item>
				<uni-grid-item>
					Vue专题
				</uni-grid-item>
				<uni-grid-item>
					Vue专题
				</uni-grid-item>
				<uni-grid-item>
					Vue专题
				</uni-grid-item>
			</uni-grid>
		</view>
	</view>
</template>

<script>
	import uniGrid from '@/components/uni-grid/uni-grid.vue'
	import uniGridItem from '@/components/uni-grid-item/uni-grid-item.vue'
	import uniNavBar from "@/components/uni-nav-bar/uni-nav-bar.vue"
	export default {
		data() {
			return {
				indicatorDots: true,
				autoplay: true,
				interval: 3000,
				duration: 500,
				name: '张三',
				day: new Date(),
				imgUrls: [
					'http://mss.sankuai.com/v1/mss_51a7233366a4427fa6132a6ce72dbe54/newsPicture/05558951-de60-49fb-b674-dd906c8897a6',
					'http://mss.sankuai.com/v1/mss_51a7233366a4427fa6132a6ce72dbe54/coursePicture/0fbcfdf7-0040-4692-8f84-78bb21f3395d',
					'http://mss.sankuai.com/v1/mss_51a7233366a4427fa6132a6ce72dbe54/management-school-picture/7683b32e-4e44-4b2f-9c03-c21f34320870'
				]
			}
		},
		methods: {},
		components: {
			uniGrid,
			uniGridItem,
			uniNavBar
		}
	}
</script>

<style lang="less">
	.container {
		background-color: #ccc;
	}

	swiper-item {
		width: 100%;
		height: 18rem;

		img {
			display: inline-block;
			width: 100%;
			height: 100%;
		}
	}

	.userinfo {
		width: 100%;
		height: 1.5rem;
		line-height: 1.5rem;
		display: flex;
		justify-content: space-between;
		margin-bottom: 10px;
		padding: 5px 10px;
		background-color: #fff;
	}

	.showinfo {
		text-align: center;
		background-color: #fff;
		padding-top: 5px;
		padding-bottom: 5px;
		margin-bottom: 10px;
	}

	.menu {
		width: 100%;
		background-color: #fff;

		uni-grid-item {
			height: 6rem;
			line-height: 6rem;
			text-align: center;
		}
	}
</style>
