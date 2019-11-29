<template>
	<div class="site">
		<nav-bar/>
		<section class="container">
			<nuxt />
		</section>
		<footer-bar/>
	</div>
</template>

<script>
	import NavBar from '~/components/NavBar.vue'
	import FooterBar from '~/components/FooterBar.vue'
	
	export default {
		components: {
			NavBar,
			FooterBar
		}
	}
</script>

<style>
	.site {
		display: flex;
		min-height: 100vh;
		flex-direction: column;
	}
	.container {
		flex: 1;
		justify-content: center;
	}
</style>

