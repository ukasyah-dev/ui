<script lang="ts">
	import type { ContainerSize } from '$lib/types/index.js';
	import type { HTMLAttributes } from 'svelte/elements';
	import { twMerge } from 'tailwind-merge';
	import Container from './Container.svelte';

	type Props = HTMLAttributes<HTMLDivElement> & {
		containerSize?: ContainerSize;
	};

	let { children, class: className, containerSize, ...rest }: Props = $props();
</script>

<Container
	class={twMerge(
		'prose prose-neutral prose-base dark:prose-invert',
		'prose-headings:font-semibold prose-headings:text-foreground-heading',
		'prose-h1:text-3xl prose-h1:mb-5 prose-h1:mt-0',
		'prose-h2:text-2xl prose-h2:mt-9',
		'prose-p:my-0 prose-p:mt-5 prose-p:text-foreground',
		'prose-a:font-medium prose-a:text-foreground-primary prose-a:underline-offset-2',
		'prose-pre:my-0 prose-pre:mt-5 prose-pre:text-base',
		'prose-code:text-foreground-semimuted',
		className?.toString()
	)}
	size={containerSize}
	{...rest}
>
	{@render children?.()}
</Container>
