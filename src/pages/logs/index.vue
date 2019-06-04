<template>
	<div>
		<div>
			<input type="text">
		</div>
		<swiper v-if="imgUrls.length > 0" indidator-dots="imgUrls.length > 1" class="pics">
			<block v-for="(item, index) in imgUrls" :key="index" >
			<swiper-item>
				<image :src="item" mode="scaleToFill" class="pic-item"></image>
			</swiper-item>
			</block>
		</swiper>
		<div class="content">
			<div class="left">
				<p @click="getItem(0)" :class="{'chooseing':isActive==0}">营养早餐</p>
				<p @click="getItem(1)" :class="{'chooseing':isActive==1}">营养早餐</p>
				<p>营养早餐</p>
				<p>营养早餐</p>
				<p>营养早餐</p>
				<p>营养早餐</p>
			</div>
			<div class="right">
				<div class="right-item" @click="jumpToDetail()">
					<img src="../../../static/images/1.jpg" alt="">
					<p>羊角面包</p>
				</div>
				<div class="right-item">
					<img src="../../../static/images/2.jpg" alt="">
					<p>羊角面包</p>
				</div>
				<div class="right-item">
					<img src="../../../static/images/2.jpg" alt="">
					<p>羊角面包</p>
				</div>
				<div class="right-item">
					<img src="../../../static/images/1.jpg" alt="">
					<p>羊角面包</p>
				</div>
				<div class="right-item">
					<img src="../../../static/images/1.jpg" alt="">
					<p>羊角面包</p>
				</div>
				<div class="right-item">
					<img src="../../../static/images/1.jpg" alt="">
					<p>羊角面包</p>
				</div>
			</div>
		</div>
		
	</div>
</template>

<script>
import { formatTime } from '@/utils/index'
export default {
	data () {
		return {
			logs: [],
			imgUrls: [
				'http://mss.sankuai.com/v1/mss_51a7233366a4427fa6132a6ce72dbe54/newsPicture/05558951-de60-49fb-b674-dd906c8897a6',
				'http://mss.sankuai.com/v1/mss_51a7233366a4427fa6132a6ce72dbe54/coursePicture/0fbcfdf7-0040-4692-8f84-78bb21f3395d',
				'http://mss.sankuai.com/v1/mss_51a7233366a4427fa6132a6ce72dbe54/management-school-picture/7683b32e-4e44-4b2f-9c03-c21f34320870'
			],
			isActive:0,
		}
	},
	methods: {
		getItem( index ){
			let _this = this;
			_this.isActive = index;
		},
		jumpToDetail(){
			wx.navigateTo({
                url:'../courseDetail/main'
            })
		}
	},

  created () {
  }
}
</script>

<style scoped lang='less'>
.pics{
	width: 100%;
}
.pic-item{
	width: 100%;
}
.content{
	display: flex;
	justify-content: flex-start;
	flex-wrap: nowrap;
	font-size: 14px;
	.left{
		width: 90px;
		p{
			width: 100%;
			height: 50px;
			line-height: 50px;
			text-align: center;
			font-size: 14px;
			border-left: 3px solid #f9f9f9;
			box-sizing: border-box;
			background-color: #f9f9f9;
		}
	}
	.right{
		padding: 20px;
		display: flex;
		justify-content:flex-start;
		flex-wrap: wrap;
		width: 260px;
		.right-item{
			width: 82px;
			text-align:center;
			img{
				width: 60px;
				height: 60px;
			}
		}
	}
}
.chooseing{
	border-left:3px solid #eb544d!important;
	background-color: white!important;
}

</style>
