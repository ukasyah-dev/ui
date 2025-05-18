<script lang="ts">
	import { Button, Container, Link, TextInput } from '$lib/index.js';
</script>

<div class="flex h-full flex-col items-center justify-center">
	<Container size="xs">
		<h1 class="text-foreground-heading mb-3 text-center text-3xl font-semibold">Welcome back</h1>
		<p class="text-foreground-semimuted mb-8 text-center">Please sign in to your account</p>

		<form class="mb-8 flex flex-col gap-6">
			<TextInput id="email" label="Email" placeholder="Your email address" />
			<TextInput id="password" label="Password" placeholder="Your password" type="password" />
			<Button class="mt-1" size="lg">Sign in</Button>
		</form>

		<p class="text-foreground-semimuted text-center">
			Don't have an account? <Link href="#register">Sign up</Link>
		</p>
	</Container>
</div>
