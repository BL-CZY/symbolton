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

    div.title {
        text-align: center;
    }

    h1 {
        font-size: 70px;
        color: rgb(152, 176, 197);
    }
</style>

<script>
    import Box from "$lib/components/box.svelte";
    import Nav from "$lib/components/nav.svelte"
    const math = ["π", "≈", "∴", "∵", "∠", "∟", "°", "⊥", "∥", "≡", "∝", "∞", "⌊⌋", "⌈⌉", "∘", "φ", "⊗", "⊆", "⊂", "⊄", "⊇", "⊃", "⊖", "∈", "∉", "¬", "⇒", "⇔", "↔"];
    const currency = ["€", "¥"];
</script>

<div class="nav">
</div>

<div class="title">
    <h1>Symbolton</h1>
</div>

<div class="main">
    <div class="sub">
        <hr/>
        {#each math as content, index}
            <div class="container">
                <Box text={content} color1="#1d813e" color2="#96ee89" color3="#00123f50"/>
            </div>
        {/each}
        <hr/>
        {#each currency as content, index}
            <div class="container">
                <Box text={content} color1="#E0AA3E" color2="#F9F295" color3="#00000050"/>
            </div>
        {/each}
    </div>
</div>
