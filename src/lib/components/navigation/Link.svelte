<script lang="ts">
	import type { HTMLAttributes } from 'svelte/elements';
	import { twMerge } from 'tailwind-merge';

	type Props = HTMLAttributes<HTMLAnchorElement> & {
		href?: string | null;
	};

	let { children, class: className, href, ...rest }: Props = $props();
</script>

<a
	{href}
	class={twMerge(
		'text-foreground-primary rounded-xs font-medium',
		'ring-offset-background focus-visible:ring-border-primary ring-0 outline-none focus-visible:ring-2 focus-visible:ring-offset-2',
		className?.toString()
	)}
	{...rest}
>
	{@render children?.()}
</a>
