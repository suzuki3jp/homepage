<script lang="ts">
	import { Content } from 'carbon-components-svelte';
	import suzuki3jp1000 from '$lib/images/suzuki3jpx1000.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="About this app" />
</svelte:head>

<Content style="text-align: center;">
	<img src={suzuki3jp1000} alt="" style="width: 180px; padding-top: 20%;" />
	<h1 style="margin-top: 3%; font-weight: bold;">suzuki3jp</h1>
	<h4 style="font-family:'Yu Gothic', '游ゴシック', YuGothic, '游ゴシック体';">
		オタクしたりゲームしたりプログラム書いたり
	</h4>
</Content>

<style>
</style>
