<script lang="ts">
	import { Typography } from '$lib/index.js';
	import MainHeader from '../MainHeader.svelte';

	let { children } = $props();
</script>

<MainHeader />

<Typography class="flex-1 py-10">
	{@render children?.()}
</Typography>
