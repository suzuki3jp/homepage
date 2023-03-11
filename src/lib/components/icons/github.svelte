<script lang="ts">
	import { ImageLoader } from 'carbon-components-svelte';
	import GitHub from '$lib/images/github.png';
	import { github } from '$lib/url.json';
</script>

<a href={github}>
	<ImageLoader src={GitHub} style="width: 30px; margin-right: 10px;" />
</a>
