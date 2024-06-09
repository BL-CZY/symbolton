<style>
    div.box {
        background: linear-gradient(to top right, var(--color-1), var(--color-2));
        display: inline-block;
        width: 10em;
        height: 10em;
        border-radius: 10px;
        transition: all 0.5s cubic-bezier(0.075, 0.82, 0.165, 1);
        justify-content: center;
    }

    div.inner {
        background-color: var(--color-3);
        border-radius: 10px;
        width: 97%;
        height: 97%;
        margin: auto;
        color: aliceblue;
    }
    
    div.holder {
        height: 1.5%;
    }
    
    div.box:hover {
        transform: scale(1.1);
    }
    
    div.space {
        height: 1.5em;
    }
    
    label {
        font-size: 35px;
        cursor: auto;
    }

    button {
        padding: 5px 10px 5px 10px;
        border: 0px;
        border-radius: 5px;
        font-size: 13px;
        transition: all 0.5s;
    }

    button:hover {
        transform: scale(1.1);
    }

    button:active {
        transform: scale(0.8);
    }
</style>

<script lang="ts">
    export let text: string;
    export let color1: string;
    export let color2: string;
    export let color3: string;

    let add_to_clipboard = () => {
        navigator.clipboard.writeText(text);
    }
</script>

<div class="box" style="--color-1: {color1}; --color-2: {color2};">
    <div class="holder"></div>
    <div class="inner" style="--color-3: {color3}">
        <div class="space"></div>
        <!-- svelte-ignore a11y-label-has-associated-control -->
        <label class="text">{text}</label><br><br>
        <button id="cp_btn" on:click={add_to_clipboard}>copy</button>
    </div>
</div>