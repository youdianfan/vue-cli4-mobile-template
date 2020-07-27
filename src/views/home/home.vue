<template>
	<div id="home">
		主页
	
	</div>
</template>

<script>
	import {Toast} from 'vant'
	import {getName} from '@/api/index'
	
	export default {
		components: {
			[Toast.name]: Toast,
		},
		data() {
			return {}
		},
		computed: {},
		created() {
			let processParams = {
				'NODE_ENV': process.env.NODE_ENV,
				'BASE_URL': process.env.BASE_URL,
				'VUE_APP_PUBLIC_PATH': process.env.VUE_APP_PUBLIC_PATH,
				'VUE_APP_API': process.env.VUE_APP_API,
			}
			console.table(processParams);
			this.getName()
		},
		mounted() {
		},
		destroyed() {
		},
		methods: {
			// 使用axios发送请求
			getName() {
				getName({
					params: 'params'
				}).then((res) => {
					console.log(res);
				}).catch((err) => {
					console.log(err);
				})
			}
		},
		watch: {}// end
	}
</script>
<style lang="less" scoped>
	#home {
	
	}
</style>

