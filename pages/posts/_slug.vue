<template>
	<div>
		<article class="message is-primary">
			<div class="message-header">
				<p>{{ post.title }}</p>
			</div>
			<div class="message-body">
				<div class="content">
					<div v-html="post.body"></div>
				</div>
				<div class="tags">
					<span v-for="(tag,index) in post.tags" :key="tag.slug + '_' + index" class="tag">{{ tag.name }}</span>
				</div>
			</div>
		</article>
		<nuxt-link to="/memo">
			<span class="icon is-small">
				<i class="fa fa-arrow-left"></i>
			</span>
		</nuxt-link>
	</div>
</template>

<script>
	import {butter} from '@/buttercms'
	
	export default {
		data() {
			return {
				post: {}
			}
		},
		methods: {
			getPost() {
				butter.post.retrieve(this.$route.params.slug)
					.then(res => {
						this.post = res.data.data
					}).catch(res => {
					console.log(res)
				})
			}
		},
		created() {
			this.getPost()
		}
	}
</script>
