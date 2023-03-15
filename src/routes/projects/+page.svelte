<script>
	import { Content } from 'carbon-components-svelte';
	import ProjectCard from './ProjectCard.svelte';
</script>

<svelte:head>
	<title>Projects</title>
	<meta name="description" content="suzuki3jp's projects" />
</svelte:head>
<div class="main-content">
	<Content>
		<h1 class="text-center" style="padding-top: 2%; font-weight: bold; margin-bottom: 2%;">
			Projects
		</h1>
		<div class="project-card-inline">
			<ProjectCard
				title="ArikenCompany"
				desc="Twitchのチャットボット<br>コメントに関する統計の収集<br>チャットコマンド、その他さまざまな機能を提供する<br><a href='https://nightbot.tv/'>Nightbot</a>をモデルに作成"
				href="https://arikencompany.github.io/"
				github="https://github.com/suzuki3jp/arikencompany"
			/>
			<ProjectCard
				title="twitch.js"
				desc="Twitchのチャットボットを作成するためのライブラリ<br>チャットボットの機能作成に関するUtilも含む<br><a href='https://github.com/twurple/twurple'>twurple</a>を拡張している"
				github="https://github.com/suzuki3jp/twitch.js"
				npm="https://www.npmjs.com/package/@suzuki3jp/twitch.js"
			/>
		</div>
		<div class="project-card-inline">
			<ProjectCard
				title="suzuki-dev.com"
				desc="Twitchの配信uptime<br>VALORANTのランクポイント<br>コンペ勝率などを日本語で返すAPI"
				github="https://github.com/suzuki3jp/suzuki-dev"
			/>
			<ProjectCard
				title="nightbot.js"
				desc="<a href='https://api-docs.nightbot.tv/'>Nightbot API</a>を操作するためのライブラリ"
				github="https://github.com/suzuki3jp/nightbot.js"
			/>
		</div>
	</Content>
</div>

<style>
	.main-content {
		width: 70%;
		margin-right: auto;
		margin-left: auto;
		margin-bottom: auto;
	}

	.project-card-inline {
		display: flex;
		margin-top: 5%;
	}

	@media (max-width: 1055px) {
		.project-card-inline {
			display: inline;
			margin-top: 5%;
		}
		.main-content {
			width: 100%;
		}
	}
</style>
