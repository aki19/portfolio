<template>
	<div>
		<div class="box">
			<article class="media">
				<div class="media-content">
					<div class="content">
						<p>
							経験言語の中ではJavaが一番好きですが、PHPでの開発経験もだいぶ増えてきました。<br/>
							マネージャー経験は最大でも10人弱くらい。<br/>
							現在は技術寄りのマネージャーとして自分とチームのスキルアップを目指す日々です。
						</p>
						<p>
							家では自分用に特化したWEBアプリ、アレクサアプリ、LINEボットを作ることにはまっています。
						</p>
					</div>
				</div>
			</article>
		</div>
		<div class="timeline">
			<header class="timeline-header">
				<span class="tag is-medium is-primary">Start</span>
			</header>
			<div class="timeline-item">
				<div class="timeline-marker is-icon">
					<i class="fa fa-flag"></i>
				</div>
				<div class="timeline-content">
					<p class="heading">April 2007</p>
					<p>ソフトウェアベンダー入社。</p>
					<p>システム寄りの製品企画や営業支援ツールの開発など。</p>
				</div>
			</div>
			<div class="timeline-item">
				<div class="timeline-marker"></div>
				<div class="timeline-content">
					<p class="heading">October 2008</p>
					<p>案件対応などを行う製品開発部署に転属。</p>
					<p>Java,XMLなど。</p>
				</div>
			</div>
			<div class="timeline-item">
				<div class="timeline-marker"></div>
				<div class="timeline-content">
					<p class="heading">April 2010</p>
					<p>企業向けシステム開発部署に転属。</p>
					<p>Java,PostgreSQLなど。</p>
				</div>
			</div>
			<div class="timeline-item">
				<div class="timeline-marker"></div>
				<div class="timeline-content">
					<p class="heading">June 2011</p>
					<p>製品開発部署に転属。</p>
					<p>C++など。</p>
				</div>
			</div>
			<div class="timeline-item">
				<div class="timeline-marker is-icon">
					<i class="fa fa-flag"></i>
				</div>
				<div class="timeline-content">
					<p class="heading">April 2012</p>
					<p>SI系企業入社。</p>
					<p>Java,Oracle SQLなど。</p>
				</div>
			</div>
			<div class="timeline-item">
				<div class="timeline-marker is-danger is-icon">
					<i class="fa fa-flag"></i>
				</div>
				<div class="timeline-content">
					<p class="heading">May 2014</p>
					<p>WEB系企業入社。</p>
					<p>Java,PHP,PostgreSQL,MySQLなど。</p>
				</div>
			</div>
			<div class="timeline-header">
				<span class="tag is-medium is-primary">Now</span>
			</div>
		</div>
	</div>
</template>

<script>
	import 'bulma-timeline/dist/css/bulma-timeline.min.css';
	
	export default {
		name: "history"
	}
</script>

<style scoped>
	.timeline {
		padding-bottom: 15px;
	}
</style>