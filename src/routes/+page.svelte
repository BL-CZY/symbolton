<style>
    div.main {
        text-align: center;
    }
    
    div.sub {
        margin: auto;
        width: 80%;
    }

    div.container {
        display: inline-block;
        padding: 1em;
    }

    div.nav {
        z-index: -1;
    }
</style>

<script>
    import Box from "$lib/components/box.svelte";
    import Nav from "$lib/components/nav.svelte"
    const math = ["±", "Ω", "β", "λ", "δ", "θ", "σ", "τ", "ω", "ɑ", "Σ", "∫", "≅", "Δ", "π", "≈", "∠", "∟", "°", "⊥", "∥", "≡", "∝", "∞", "⌊⌋", "⌈⌉", "∘", "φ", "⊗", "⊆", "⊂", "⊄", "⊇", "⊃", "⊖", "∈", "∉", "¬", "⇒", "⇔", "↔", "∴", "∵"];
    const currency = ["€", "β", "λ", "δ", "θ", "σ", "τ", "ω", "ɑ", "Σ", "∫"];
</script>

<div class="nav">
</div>

<div class="main">
    <div class="sub">
        {#each math as content, index}
            <div class="container">
                <Box text={content} color1="#1d813e" color2="#96ee89" color3="#00123f50"/>
            </div>
        {/each}
        <hr />
        {#each currency as content, index}
            <div class="container">
                <Box text={content} color1="#E0AA3E" color2="#F9F295" color3="#00000050"/>
            </div>
        {/each}
    </div>
</div>
