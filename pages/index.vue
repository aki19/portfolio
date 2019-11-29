<template>
	<div class="has-text-centered">
		<section class="hero">
			<div class="hero-body">
				<div class="container has-text-centered">
					<h1 class="title">
						portfolio
					</h1>
				</div>
			</div>
		</section>
		<div class="container">
			<div class="tile is-ancestor">
				<div class="tile is-parent is-8">
					<article class="tile is-child box">
						<div class="content">
							<profile/>
						</div>
					</article>
				</div>
				<div class="tile is-parent">
					<article class="tile is-child notification is-primary">
						<div class="content is-large main-link">
							<ul class="is-unstyled">
								<li>
								<span class="icon">
									<i class="fa fa-home"></i>
								</span>
									<a href="http://alicesystems.lomo.jp/wp/" target="_blank" style="text-decoration: none;">AliceSystems</a>
								</li>
							</ul>
						</div>
						<div class="content is-medium sub-link">
							<ul class="is-unstyled">
								<li v-for="item in items" :key="item.title">
								<span class="icon">
									<i :class="item.icon"></i>
								</span>
									<a :href="item.url" target="_blank" style="text-decoration: none;">
										{{ item.title }}
									</a>
								</li>
							</ul>
						</div>
					</article>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	import Profile from '~/components/Profile.vue'
	
	export default {
		components: {
			Profile
		},
		data: () => ({
			items: [
				{title: 'booklog', icon: 'fa fa-book', url: 'https://booklog.jp/users/aki19'},
				{title: 'Tumblr', icon: 'fa fa-tumblr-square', url: 'http://aki19.tumblr.com/'},
				{title: 'Hatena Bookmark', icon: 'fa fa-bookmark', url: 'http://b.hatena.ne.jp/akikara/'}
			]
		})
	}
</script>

<style>
	.title {
		font-size: 5rem;
		letter-spacing: 1px;
		padding-top: 30px;
		padding-bottom: 30px;
	}
	
	.main-link {
		padding-top: 15px;
	}
	
	ul.is-unstyled {
		list-style: none;
		margin: 0;
		padding: 0;
	}
	
	.sub-link {
		padding-bottom: 15px;
	}
</style>

