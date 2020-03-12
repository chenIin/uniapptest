<template>
	<view class="content">
		
		<input v-model="test" value="" />
		 <text >{{test}}</text>
		<button @click="testfu">dfdfdd</button>
		
		
		
	</view>
</template>

<script>
	import uniGrid  from '../../components/uni-grid/uni-grid.vue'
	import uniGridItem from "@/components/uni-grid-item/uni-grid-item.vue"
	export default {
		data() {
			return {
				test:"我是你爸爸"
			}
		},
		onLoad() {
			console.log("dfdef33")
			uni.getLocation({
			    type: 'wgs84',
			    success: function (res) {
			        console.log('当前位置的经度：' + res.longitude);
			        console.log('当前位置的纬度：' + res.latitude);
					      console.log('当前位置的纬度23：' + res.latitude);
			    }
			});
			
			
			
		},
		methods: {
            testfu:function(){
			this.test="djksf3"
			}

		},
		components:{
			uniGrid,uniGridItem
		}
	}
</script>

<style>
	.intro {
		font-size: 14px;
		line-height: 24px;
	}
</style>
