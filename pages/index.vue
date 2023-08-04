<template>
	
	<view class="container">
		
	
		<view class="flex diygw-col-24 flex-direction-column">
			<scroll-view scroll-x :scroll-into-view="'scroll-' + tabsIndex" scroll-with-animation class="diygw-tabs text-center justify-start scale-title small-border">
				<view :id="'scroll-' + index" class="diygw-tab-item" :class="index == tabsIndex ? 'cur text-green' : ''" v-for="(item, index) in tabsDatas" :key="index" @click="changeTabs" :data-index="index">
					{{ item.text }}
				</view>
			</scroll-view>
		</view>
		<view class="flex diygw-col-24">
			<view class="diygw-pzx" style="border-bottom: 10px solid #eee"></view>
		</view>
		
		
		
		
	
		
		
		
		<view class="flex diygw-col-24 swiper1-clz">
			<swiper class="swiper" indicator-dots="true" autoplay interval="3000" circular="true" style="height: 150px">
				<swiper-item class="diygw-swiper-item">
					<view class="diygw-swiper-item-wrap">
						<image src="/static/banner-1.png" class="diygw-swiper-image"></image>
						<view class="diygw-swiper-item-title">  </view>
					</view>
				</swiper-item>
				<swiper-item class="diygw-swiper-item">
					<view class="diygw-swiper-item-wrap">
						<image src="/static/banner-2.png" class="diygw-swiper-image"></image>
						<view class="diygw-swiper-item-title">  </view>
					</view>
				</swiper-item>
				<swiper-item class="diygw-swiper-item">
					<view class="diygw-swiper-item-wrap">
						<image src="/static/banner-3.png" class="diygw-swiper-image"></image>
						<view class="diygw-swiper-item-title">  </view>
					</view>
				</swiper-item>
			</swiper>
		</view>
		
		
		
		
		
		<view class="flex diygw-col-24">
			<diy-noticebar class="flex1 diy-notice-bar" color="#07c160" bgColor="#fff" leftIcon="diy-icon-notification">
				<!-- #ifndef VUE3 -->
				<block slot="content">
					<text class="diy-notice-item">ยินดีต้อนรับเข้าสู่ GM-TH แพลตฟอร์มสร้างรายได้ออนไลน์</text>
				</block>
				<!-- #endif -->
				<!-- #ifdef VUE3 -->
				<block v-slot:content>
					<text class="diy-notice-item"> ยินดีต้อนรับเข้าสู่ GM-TH แพลตฟอร์มสร้างรายได้ออนไลน </text>
				</block>
				<!-- #endif -->
			</diy-noticebar>
		</view>
	






		
				
	


		

	
	
	
	
	
	
		<view class="clearfix"></view>
	</view>
</template>

<script>
	//create by: 邓志锋 <280160522@qq.com> <https://www.diygw.com> DIYGW可视化设计一键生成源码
	export default {
		data() {
			return {
				search: '',
				tabsDatas: [{ text: `หน้าแรก` }, { text: `ดูหนังออนไลน์` }, { text: `ดูบอล` }, { text: `เครดิตฟรี` }, { text: `ทายบอล` }, { text: `เงื่อนไข` }],
				tabsIndex: 0,
				modal: ''
			};
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
			async init() {},
			changeTabs(evt) {
				let { index } = evt.currentTarget.dataset;
				if (index == this.tabsIndex) return;
				this.setData({
					tabsIndex: index
				});
			}
		}
	};
</script>

<style lang="scss" scoped>
	
	.audio-clz {
		margin-left: 5px;
		width: calc(100% - 5px - 5px) !important;
		margin-top: 5px;
		margin-bottom: 5px;
		margin-right: 5px;
	}
	.container {
		padding-bottom: 80px;
	}

</style>
