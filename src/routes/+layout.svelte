<script lang="ts">
	import { page } from '$app/stores';
	import HOME_ICON from '$lib/components/icons/home.svelte';
	import LINKS_ICON from '$lib/components/icons/links.svelte';
	import PROJECTS_ICON from '$lib/components/icons/projects.svelte';
	import GITHUB_ICON from '$lib/components/icons/github.svelte';
	import TWITTER_ICON from '$lib/components/icons/twitter.svelte';
	import suzuki3jp_icon from '$lib/images/suzuki3jp-icon.png';
	import { twitter, github } from '$lib/url.json';

	import {
		Header,
		ImageLoader,
		SideNav,
		SideNavItems,
		SideNavLink,
		SideNavMenu,
		SkipToContent,
		Content
	} from 'carbon-components-svelte';
	import 'carbon-components-svelte/css/g90.css';

	let isSideNavOpen = false;
</script>

<div class="app">
	<Header bind:isSideNavOpen style="display: none;">
		<img src={suzuki3jp_icon} alt="suzuki3jp icon" style="width: 25px; margin-left: 12px;" />
		<div style="margin-left: 10px">鈴木 (suzuki3jp)</div>
		<svelte:fragment slot="skip-to-content">
			<SkipToContent />
		</svelte:fragment>
		<div style="margin: 0 0 0 auto;">
			<GITHUB_ICON />
			<TWITTER_ICON />
		</div>
	</Header>

	<SideNav bind:isOpen={isSideNavOpen} rail>
		<SideNavItems>
			<SideNavLink icon={HOME_ICON} text="HOME" href="/" isSelected={$page.url.pathname === '/'} />
			<SideNavLink
				icon={PROJECTS_ICON}
				text="PROJECTS"
				href="/projects"
				isSelected={$page.url.pathname === '/projects'}
			/>
			<SideNavMenu icon={LINKS_ICON} text="LINKS">
				<SideNavLink text="Twitter" href={twitter} style="font-weight: bold;" />
				<SideNavLink text="GitHub" href={github} style="font-weight: bold;" />
			</SideNavMenu>
		</SideNavItems>
	</SideNav>

	<main>
		<slot />
	</main>

	<footer>
		<Content>
			Copyright (c) <a href={github}>suzuki3jp</a> All Rights Reserved
		</Content>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
