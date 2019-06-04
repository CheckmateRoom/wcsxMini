<template>
	<div>
		<!-- <img :src="imgUrl" alt=""> -->
		<img src="../../../static/images/background.jpg" alt="">
	</div>
</template>

<script>
export default {
	data () {
		return {
			imgUrl:"../../../static/images/background.jpg"
		}
	},
  	methods: {
	},

	created () {
		// let app = getApp()
	}
}
</script>

<style scoped>
	img{
		width: 100%;
		height: 825px;
	}
</style>
