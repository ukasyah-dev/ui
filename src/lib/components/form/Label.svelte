<script lang="ts">
	import type { HTMLLabelAttributes } from 'svelte/elements';
	import { twMerge } from 'tailwind-merge';

	type Props = HTMLLabelAttributes;

	let { children, class: className, ...rest }: Props = $props();
</script>

<label
	class={twMerge(
		'text-foreground-semimuted mb-1 block text-base font-medium',
		className?.toString()
	)}
	{...rest}
>
	{@render children?.()}
</label>
