<template>
	<div id="error">
		<van-empty image="error" description="error Page" />
	</div>
</template>

<script>
	import {Empty} from 'vant'
	
	export default {
		name: "error",
		components: {
			[Empty.name]: Empty,
		}
	}
</script>
