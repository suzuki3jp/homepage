<script lang="ts">
	import GitHub from '$lib/images/github.png';
	import Links from '$lib/images/links-icon.png';
	import Npm from '$lib/images/npm.png';
	export let title: string;
	export let desc: string | undefined = undefined;
	export let href: string | undefined = undefined;
	export let github: string | undefined = undefined;
	export let npm: string | undefined = undefined;
</script>

<div class="project-card">
	<h2 class="text-center" style="font-weight: 500; margin: 5px 0 10px 0;">{title}</h2>
	{#if desc}
		<div style="margin-left: 5%; font-size: 15px; line-height: 20px">{@html desc}</div>
	{/if}
	<div class="project-card-links">
		{#if href}
			<a {href} class="project-card-links-margin">
				<img src={Links} alt="links icon" style="width: 30px;" /></a
			>
		{/if}
		{#if github}
			<a href={github} class="project-card-links-margin">
				<img src={GitHub} alt="github logo" style="width: 30px;" />
			</a>
		{/if}
		{#if npm}
			<a href={npm} class="project-card-links-margin">
				<img src={Npm} alt="npm logo" style="width: 30px" />
			</a>
		{/if}
	</div>
</div>

<style>
	.project-card {
		border-color: white;
		border-width: 2px;
		border-style: solid;
		width: 50%;
		background-color: #4c4c4c;
		padding: 5px 0 5px 0;
		margin-right: 5%;
		height: fit-content;
	}

	.project-card-links {
		margin-left: auto;
		width: fit-content;
		margin-right: 6%;
		display: flex;
	}

	.project-card-links-margin {
		margin-left: 10%;
	}
	@media (max-width: 1055px) {
		.project-card {
			width: 80%;
			margin-top: 5%;
			margin-left: auto;
			margin-right: auto;
		}
	}
	@media (max-width: 400px) {
		.project-card {
			width: 90%;
			margin-top: 5%;
			margin-left: auto;
			margin-right: auto;
		}
	}
</style>
