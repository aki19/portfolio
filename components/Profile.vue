<template>
	<div>
		<article class="media">
			<figure class="media-left">
				<p class="image is-96x96">
					<img class="is-rounded" src="@/assets/myicon_108.png" alt="aki19 image">
				</p>
			</figure>
			<div class="media-content">
				<div class="content">
					<p>
						<strong>aki19</strong>
						<br>
						東京在住。プログラマやってます。<br/>
						新しいサービスやソフトを試すのが大好き！<br/>
						コンタクトはTwitterでお願いします。<br/><br/>
						本サイトはNuxt.js＋Bulmaで作りました。
					</p>
				</div>
				<nav class="level is-mobile">
					<div class="level-left">
						<a class="level-item" href="http://twitter.com/#!/aki19" target="_blank">
							<span class="icon is-small"><i class="fa fa-twitter"></i></span>
						</a>
					</div>
				</nav>
			</div>
		</article>
	</div>
</template>

<script>
	export default {
		name: "Profile"
	}
</script>

<style scoped>
	.media {
		font-family: 'Kosugi Maru', sans-serif;
	}
</style>