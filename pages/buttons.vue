<template>
	<view class="container">
		<view class="flex diygw-col-24 diygw-bottom">
			<view class="diygw-grid diygw-actions">
				<button class="diygw-action">
					<view class="diygw-grid-inner">
						<view class="diygw-grid-icon diygw-avatar">
							<image mode="aspectFit" class="diygw-avatar-img" src="/static/grid1.png"></image>
						</view>
						<view class="diygw-grid-title"> หน้าหลัก </view>
					</view>
				</button>
				<button class="diygw-action">
					<view class="diygw-grid-inner">
						<view class="diygw-grid-icon diygw-avatar">
							<image mode="aspectFit" class="diygw-avatar-img" src="/static/grid2.png"></image>
						</view>
						<view class="diygw-grid-title"> ภารกิจ </view>
					</view>
				</button>
				<button class="diygw-action addon">
					<view class="diygw-grid-inner">
						<view class="diygw-grid-icon diygw-avatar">
							<image mode="aspectFit" class="diygw-avatar-img" src="/static/logo.png"></image>
						</view>
						<view class="diygw-grid-title"> โบนัส </view>
					</view>
				</button>
				<button class="diygw-action">
					<view class="diygw-grid-inner">
						<view class="diygw-grid-icon diygw-avatar">
							<image mode="aspectFit" class="diygw-avatar-img" src="/static/grid3.png"></image>
						</view>
						<view class="diygw-grid-title"> แชทสด </view>
					</view>
				</button>
				<button class="diygw-action">
					<view class="diygw-grid-inner">
						<view class="diygw-grid-icon diygw-avatar">
							<image mode="aspectFit" class="diygw-avatar-img" src="/static/grid4.png"></image>
						</view>
						<view class="diygw-grid-title"> ข้อมูล </view>
					</view>
				</button>
			</view>
		</view>
	
		<view class="clearfix"></view>
	</view>
</template>

<script>
	//create by: 邓志锋 <280160522@qq.com> <https://www.diygw.com> DIYGW可视化设计一键生成源码
	export default {
		data() {
			return {};
		},
		onShareAppMessage: function () {},
		onLoad(option) {
			this.setCurrentPage(this);
			if (option) {
				this.setData({
					globalOption: option
				});
			}
		},
		mounted() {
			this.init();
		},
		methods: {
			async init() {}
		}
	};
</script>

<style lang="scss" scoped>
	.container {
		padding-bottom: 80px;
	}
</style>
