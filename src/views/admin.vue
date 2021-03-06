<template>
	<v-app>
		<Nav />
		<v-main>
			<router-view></router-view>
		</v-main>
	</v-app>
</template>

<script>
//	import Nav from '@/components/nav.vue'
  import Nav from '@/components/player.vue'
	export default {
		components:{
			Nav
		}
	}
</script>

<style>
</style>
