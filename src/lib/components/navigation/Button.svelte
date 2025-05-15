<script lang="ts">
	import type { HTMLButtonAttributes } from 'svelte/elements';
	import { twMerge } from 'tailwind-merge';

	type Props = HTMLButtonAttributes & {
		square?: boolean;
		variant?: 'ghost';
	};

	let { children, class: className, square, variant = 'ghost', ...rest }: Props = $props();

	let _class = twMerge(
		'cursor-pointer flex items-center justify-center',
		'transition duration-100',
		square && 'px-0 w-8 h-8 rounded-lg',
		variant === 'ghost' && 'hover:bg-background-semimuted',
		className?.toString()
	);
</script>

<button class={_class} {...rest}>
	{@render children?.()}
</button>
