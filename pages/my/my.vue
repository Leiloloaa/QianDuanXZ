<template>
	<view class="container">
		<view class="showInfo">
			<button class="mini-btn" plain="true" size="mini">登录/注册</button>
		</view>

		<uni-list>
			<uni-list-item title="个人信息">
				<template v-slot:right="">
					<image style="width: 20px;height: 20px;" src="/static/info.png" mode="widthFix"></image>
				</template>
			</uni-list-item>
			<uni-list-item title="我的订单">
				<template v-slot:right="">
					<image style="width: 20px;height: 20px;" src="/static/order.png" mode="widthFix"></image>
				</template>
			</uni-list-item>
			<uni-list-item title="联系我们">
				<template v-slot:right="">
					<image style="width: 20px;height: 20px;" src="/static/wu.png" mode="widthFix"></image>
				</template>
			</uni-list-item>
		</uni-list>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			};
		}
	}
</script>

<style lang="less">
	.container {
		.showInfo {
			width: 100%;
			height: 6rem;
			background-color: #18b4ed;
			position: relative;

			button {
				position: absolute;
				display: block;
				color: #fff;
				top: 50%;
				left: 50%;
				transform: translate(-50%, -50%);
			}
		}
	}
</style>
