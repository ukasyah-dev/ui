<script lang="ts">
	import { Button, Container, title } from '$lib/index.js';
	import MainHeader from './MainHeader.svelte';

	title.reset();
</script>

<MainHeader />

<Container class="flex flex-1 flex-col items-center justify-center">
	<h1 class="text-foreground-heading mb-4 text-3xl font-semibold">
		Lightweight and modern UI library for Svelte
	</h1>
	<p
		class="text-foreground-semimuted mx-auto mb-8 w-full max-w-2xl text-center text-lg leading-normal"
	>
		Built to accelerate Svelte app development with ready-to-use, themeable components that let you
		ship faster with confidence.
	</p>
	<div class="flex gap-4">
		<Button href="/docs/getting-started" size="lg">Get started</Button>
		<Button href="/docs/components" size="lg" variant="secondary">Browse components</Button>
	</div>
</Container>
