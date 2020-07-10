<script>
	import Tailwindcss from './Tailwindcss.svelte';
</script>

<main>
	<Tailwindcss />

	<h1>Hello world!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
</main>

<style type="text/scss">
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		font-family: 'Segoe UI', sans-serif;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-weight: 100;
		padding: 1rem 0;
		position: relative;
		@apply text-6xl;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
