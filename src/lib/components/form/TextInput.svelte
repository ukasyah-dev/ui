<script lang="ts">
	import type { HTMLInputAttributes } from 'svelte/elements';
	import Label from './Label.svelte';
	import Input from './Input.svelte';

	type Props = HTMLInputAttributes & {
		id: string;
		label: string;
	};

	let { id, label, ...rest }: Props = $props();
</script>

<div>
	<Label for={id}>{label}</Label>
	<Input {id} {...rest} />
</div>
