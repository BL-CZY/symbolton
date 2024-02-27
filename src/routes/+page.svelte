<style>
    div.main {
        text-align: center;;
    }
    div.container {
        display: inline-block;
        padding: 10px;
    }
</style>

<script>
    import Box from "$lib/components/box.svelte";
    const math = ["Ω", "β", "λ", "δ", "θ", "σ", "τ", "ω", "ɑ", "Σ", "∫"];
</script>

<div class="main">
    {#each math as content, index}
        <div class="container">
            <Box text={content}/>
        </div>
    {/each}
</div>