<script>
	export let counter;

	$: percent = counter * 5;
</script>

<div class="my-4 shadow w-full bg-gray-400">
	<div class="bg-green-500 text-sm leading-none py-3 text-center text-white progress" style="width: {percent}%">
		{counter < 20 ? counter > 2 ? counter + " seconds left" : counter > 0 ? counter : "" : ""}
	</div>
</div>

<style type="text/scss">
	.progress{
		transition: 1s;
	}
</style>
