<template>
	<nav class="navbar is-primary">
		<div class="navbar-brand">
			<nuxt-link class="navbar-item" to="/">
				<span class="site-title">aki19@AliceSystems</span>
			</nuxt-link>
			<div class="navbar-burger burger burger-font-icon" @click="showNav = !showNav"
				 :class="{'is-active': showNav}">
				<img src="@/assets/baseline-menu-24px.svg"/>
			</div>
		</div>
		<div id="navbarExampleTransparentExample" class="navbar-menu" :class="{'is-active':showNav}">
			<div class="navbar-start">
				<nuxt-link v-for="item in items" :key="item.title" :to="item.url" class="navbar-item">
					{{ item.title }}
				</nuxt-link>
			</div>
			<div class="navbar-end">
				<div class="navbar-item">
					<div class="field is-grouped">
						<p class="control">
							<a class="bd-tw-button button is-primary is-inverted"
							   data-social-network="Twitter" data-social-action="tweet"
							   data-social-target="http://alicesystems.lomo.jp/portfolio" target="_blank"
							   href="https://twitter.com/intent/tweet?text=aki19@AliceSystems&amp;url=http://alicesystems.lomo.jp/portfolio">
								<span class="icon">
									<i class="fa fa-twitter"></i>
								</span>
								<span>Tweet</span>
							</a>
						</p>
					</div>
				</div>
			</div>
		</div>
	</nav>
</template>

<script>
	import memo from '~/pages/memo.vue'
	import history from '~/pages/history.vue'
	
	export default {
		name: "NavBar",
		components: {
			memo,
			history
		},
		data: () => ({
			showNav: false,
			items: [
				{title: 'Home', url: '/'},
				{title: 'Memo', url: '/memo'},
				{title: 'History', url: '/history'}
			]
		})
	}
</script>

<style scoped>
	.navbar {
		margin-bottom: 20px;
	}
	
	.burger-font-icon img {
		height: 30px;
		margin: 10px 0 0 12px;
	}
	
	.site-title {
		font-family: 'Ribeye', cursive;
	}
</style>