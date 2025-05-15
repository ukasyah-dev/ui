<script lang="ts">
	import { Container, title } from '$lib/index.js';
	import MainHeader from './MainHeader.svelte';

	title.reset();
</script>

<MainHeader />

<Container class="flex flex-1 flex-col items-center justify-center">
	<h1 class="mb-4 text-3xl font-semibold">Lightweight and modern UI library for Svelte</h1>
	<p class="mx-auto w-full max-w-2xl text-center text-lg leading-normal">
		Built to accelerate Svelte app development with ready-to-use, themeable components that let you
		ship faster with confidence.
	</p>
</Container>
