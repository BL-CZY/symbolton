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
    }
    </style>

<script>
    export let text;
    export let color1;
    export let color2;
    export let color3;
</script>

<div class="box" style="--color-1: {color1}; --color-2: {color2};">
    <div class="holder"></div>
    <div class="inner" style="--color-3: {color3}">
        <div class="space"></div>
        <!-- svelte-ignore a11y-label-has-associated-control -->
        <label class="text">{text}</label><br>
        <button id="cp_btn">copy to clipboard</button>
    </div>
</div>