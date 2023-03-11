<script lang="ts">
	import { ImageLoader } from 'carbon-components-svelte';
	import Twitter from '$lib/images/twitter.png';
	import { twitter } from '$lib/url.json';
</script>

<a href={twitter}>
	<ImageLoader src={Twitter} style="width: 30px; margin-right: 10px;" />
</a>
