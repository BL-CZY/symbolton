<style>
    div.box {
        background-color: aliceblue;
        display: inline-block;
        width: 10em;
        height: 10em;
        border-radius: 10px;
    }

    div.space {
        height: 1.5em;
    }

    label {
        font-size: 35px;
    }
</style>

<script>
    export let text;
</script>

<div class="box">
    <div class="space"></div>
    <!-- svelte-ignore a11y-label-has-associated-control -->
    <label class="text">{text}</label><br>
    <button>copy to clipboard</button>
</div>