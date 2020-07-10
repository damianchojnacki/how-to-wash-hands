<script>
    import { fade } from 'svelte/transition';

    export let counter, countDown;

    $: backgroundAndColor = counter > 0 ? "bg-gray-400" : "bg-green-500 text-white";
    $: disabled = counter < 20 && counter > 0;
</script>


{#if !disabled}
    <button class="{backgroundAndColor} px-4 py-2 rounded" on:click={countDown} disabled={disabled} transition:fade>
        {counter > 0 ?
                "Start washing"
            :
                "Done!"
            }
    </button>
{/if}
