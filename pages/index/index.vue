<template>	
	<view class="content animated fadeInRight">
		<!-- hover-class点击后的样式，会变回来 -->
		<!-- hover-stay-time 点击后样式的持续时间 -->
		<!-- @tap和@click一样也是点击事件，不过在移动端推荐使用tap，肯呢个是因为快点吧 -->
		<view hover-class="hoverItem rubberBand" class="item animated" :hover-stay-time="800" @tap="animated">
			
		</view>
	</view>
</template>

<script>
	// import topBar from '../../common/topBar/topBar.vue'
	export default {
		data() {
			return {
				title: 'Hello',
				animate:false
			}
		},
		onLoad() {

		},
		created() {

		},
		methods: {
			animated(e) {
				console.log('sasas');
			}
		},
		components:{
			// topBar
		}
	}
</script>

<style scoped lang="less">
.content{
	.item{
		width: 200upx;
		height: 200upx;
		background-color: #000;
		margin-top: 50upx;
	}
	
	.hoverItem{
		background-color: red;
	}
}

</style>
