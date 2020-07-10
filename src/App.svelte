<script>
	import Tailwindcss from './Tailwindcss.svelte';
	import Countdown from "./Countdown.svelte";
	import Button from "./Button.svelte";

	let counter = 20;

	function countDown() {
		setTimeout(() => {
			counter--;

			counter > 0 && countDown();
		}, 1000);
	}
</script>

<main class="w-full md:w-1/2 mx-auto min-h-screen flex flex-col justify-center items-center">
	<Tailwindcss/>

	<h1 class="text-center text-2xl md:text-6xl">How to wash hands?</h1>

	<Countdown {counter}/>

	<Button {counter} {countDown}/>
</main>

<style type="text/scss">

</style>
