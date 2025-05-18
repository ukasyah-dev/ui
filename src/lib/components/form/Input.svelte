<script lang="ts">
	import type { HTMLInputAttributes } from 'svelte/elements';
	import { twMerge } from 'tailwind-merge';

	type Props = HTMLInputAttributes;

	let { class: className, ...rest }: Props = $props();
</script>

<input
	class={twMerge(
		'w-full',
		'placeholder:text-foreground-muted',
		'bg-background-semimuted border-border text-foreground',
		'focus:border-border-primary focus:ring-border-primary',
		'h-11 rounded-md px-4',
		className?.toString()
	)}
	{...rest}
/>
