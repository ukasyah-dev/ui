<script lang="ts">
	import type { HTMLAttributes, HTMLButtonAttributes } from 'svelte/elements';
	import { twMerge } from 'tailwind-merge';

	type Props = HTMLButtonAttributes &
		HTMLAttributes<HTMLAnchorElement> & {
			href?: string;
			square?: boolean;
			variant?: 'ghost';
		};

	let { children, class: className, href, square, variant = 'ghost', ...rest }: Props = $props();

	let _class = twMerge(
		'cursor-pointer flex items-center justify-center',
		'transition duration-100',
		square && 'px-0 w-8 h-8 rounded-lg',
		variant === 'ghost' && 'hover:bg-background-semimuted',
		className?.toString()
	);
</script>

{#if href}
	<a class={_class} {href} {...rest}>
		{@render children?.()}
	</a>
{:else}
	<button class={_class} {...rest}>
		{@render children?.()}
	</button>
{/if}
