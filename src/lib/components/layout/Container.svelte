<script lang="ts">
	import type { ContainerSize } from '$lib/types/index.js';
	import type { HTMLAttributes } from 'svelte/elements';
	import { twMerge } from 'tailwind-merge';

	type Props = HTMLAttributes<HTMLDivElement> & {
		size?: ContainerSize;
	};

	let { children, class: className, size = 'md', ...rest }: Props = $props();
</script>

<div
	class={twMerge(
		'mx-auto w-full px-6',
		size === 'xs' && 'max-w-90',
		size === 'sm' && 'max-w-xl',
		size === 'md' && 'max-w-3xl',
		size === 'lg' && 'max-w-5xl',
		size === 'xl' && 'max-w-6xl',
		className?.toString()
	)}
	{...rest}
>
	{@render children?.()}
</div>
