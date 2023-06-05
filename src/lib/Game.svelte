<script lang="ts">
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();

    export let correctWord: {id: number, word: string};
    export let turn: number = 0;
    export let isCorrect: boolean = false;
    export let gameOver = false;
    export let currentGuess: string = "";
    export let guesses: {letter: string, color: string}[][] = [
        [
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
        ],
        [
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
        ],
        [
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
        ],
        [
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
        ],
        [
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
        ],
        [
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
            {letter: "", color: ""},
        ],
    ];
    export let history: string[] = [];

    const addGuess = () => dispatch("addGuess");
    const formatGuess = () => dispatch("formatGuess");
    // const handleInput = () => dispatch("handleInput");

    console.log("%cWordle", "color: #6aaa64; font-weight: bold; font-size: 30px");
    console.log("%cCreated By: Parteek Deol", "font-weight: bold; font-size: 15px");
    console.log("The answer is: " + correctWord.word + " :)");
</script>

<div id="game">
    <div>
        { #each guesses as guess }
            { #if guess }
                <div class="row entered-row">
                    { #if turn == guesses.indexOf(guess) }
                        { #each [...currentGuess] as guessElm }
                            <div>{guessElm}</div>
                        { /each }
                        { #each [...Array(5 - currentGuess.length)] as emptyElm}
                            <div></div>
                        { /each }
                    { :else }
                        { #each guess as guessElm }
                            <div class={guessElm.color}>{guessElm.letter}</div>
                        { /each }
                    { /if }
                </div>
            { :else }
                <div class="row empty-row">
                    <div></div>
                    <div></div>
                    <div></div>
                    <div></div>
                    <div></div>
                    <div></div>
                </div>
            { /if }
        { /each }
    </div>
</div>

<style>
    .green {
        background-color: #6aaa64;
        color: white;
    }
    .yellow {
        background-color: #f7da21;
        color: white;
    }
    .gray {
        background-color: #86888a;
        color: white;
    }
</style>