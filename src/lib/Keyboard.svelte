<script lang="ts">
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();

    const handleInput = (e) => dispatch("handleInput", { key: e.srcElement.id });
</script>

<div id="keyboard">
    <div id="row-1">
        <button class="key" id="q" on:click={(e) => handleInput(e)}>Q</button>
        <button class="key" id="w" on:click={(e) => handleInput(e)}>W</button>
        <button class="key" id="e" on:click={(e) => handleInput(e)}>E</button>
        <button class="key" id="r" on:click={(e) => handleInput(e)}>R</button>
        <button class="key" id="t" on:click={(e) => handleInput(e)}>T</button>
        <button class="key" id="y" on:click={(e) => handleInput(e)}>Y</button>
        <button class="key" id="u" on:click={(e) => handleInput(e)}>U</button>
        <button class="key" id="i" on:click={(e) => handleInput(e)}>I</button>
        <button class="key" id="o" on:click={(e) => handleInput(e)}>O</button>
        <button class="key" id="p" on:click={(e) => handleInput(e)}>P</button>
    </div>
    <div id="row-2">
        <button class="key" id="a" on:click={(e) => handleInput(e)}>A</button>
        <button class="key" id="s" on:click={(e) => handleInput(e)}>S</button>
        <button class="key" id="d" on:click={(e) => handleInput(e)}>D</button>
        <button class="key" id="f" on:click={(e) => handleInput(e)}>F</button>
        <button class="key" id="g" on:click={(e) => handleInput(e)}>G</button>
        <button class="key" id="h" on:click={(e) => handleInput(e)}>H</button>
        <button class="key" id="j" on:click={(e) => handleInput(e)}>J</button>
        <button class="key" id="k" on:click={(e) => handleInput(e)}>K</button>
        <button class="key" id="l" on:click={(e) => handleInput(e)}>L</button>
    </div>
    <div id="row-3">
        <button class="key" id="Enter" on:click={(e) => handleInput(e)}>Enter</button>
        <button class="key" id="z" on:click={(e) => handleInput(e)}>Z</button>
        <button class="key" id="x" on:click={(e) => handleInput(e)}>X</button>
        <button class="key" id="c" on:click={(e) => handleInput(e)}>C</button>
        <button class="key" id="v" on:click={(e) => handleInput(e)}>V</button>
        <button class="key" id="b" on:click={(e) => handleInput(e)}>B</button>
        <button class="key" id="n" on:click={(e) => handleInput(e)}>N</button>
        <button class="key" id="m" on:click={(e) => handleInput(e)}>M</button>
        <button class="key" id="Backspace" on:click={(e) => handleInput(e)}>Delete</button>
    </div>
</div>