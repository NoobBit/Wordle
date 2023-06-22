<script lang="ts">
	import {v4 as uuidv4} from "uuid";

	import Game from "./lib/Game.svelte";
    import Modal from "./lib/Modal.svelte";
    import Keyboard from "./lib/Keyboard.svelte";

	let words: {id: number, word: string}[] = [
		{id: uuidv4(), word: "about"},
        {id: uuidv4(), word: "alert"},
        {id: uuidv4(), word: "argue"},
        {id: uuidv4(), word: "beach"},
        {id: uuidv4(), word: "above"},
        {id: uuidv4(), word: "alike"},
        {id: uuidv4(), word: "arise"},
        {id: uuidv4(), word: "began"},
        {id: uuidv4(), word: "abuse"},
        {id: uuidv4(), word: "alive"},
        {id: uuidv4(), word: "array"},
        {id: uuidv4(), word: "begin"},
        {id: uuidv4(), word: "actor"},
        {id: uuidv4(), word: "allow"},
        {id: uuidv4(), word: "aside"},
        {id: uuidv4(), word: "begun"},
        {id: uuidv4(), word: "acute"},
        {id: uuidv4(), word: "alone"},
        {id: uuidv4(), word: "asset"},
        {id: uuidv4(), word: "being"},
        {id: uuidv4(), word: "admit"},
        {id: uuidv4(), word: "along"},
        {id: uuidv4(), word: "audio"},
        {id: uuidv4(), word: "below"},
        {id: uuidv4(), word: "adopt"},
        {id: uuidv4(), word: "alter"},
        {id: uuidv4(), word: "audit"},
        {id: uuidv4(), word: "bench"},
        {id: uuidv4(), word: "adult"},
        {id: uuidv4(), word: "among"},
        {id: uuidv4(), word: "avoid"},
        {id: uuidv4(), word: "billy"},
        {id: uuidv4(), word: "after"},
        {id: uuidv4(), word: "anger"},
        {id: uuidv4(), word: "award"},
        {id: uuidv4(), word: "birth"},
        {id: uuidv4(), word: "again"},
        {id: uuidv4(), word: "angle"},
        {id: uuidv4(), word: "aware"},
        {id: uuidv4(), word: "black"},
        {id: uuidv4(), word: "agent"},
        {id: uuidv4(), word: "angry"},
        {id: uuidv4(), word: "badly"},
        {id: uuidv4(), word: "blame"},
        {id: uuidv4(), word: "agree"},
        {id: uuidv4(), word: "apart"},
        {id: uuidv4(), word: "baker"},
        {id: uuidv4(), word: "blind"},
        {id: uuidv4(), word: "ahead"},
        {id: uuidv4(), word: "apple"},
        {id: uuidv4(), word: "bases"},
        {id: uuidv4(), word: "block"},
        {id: uuidv4(), word: "alarm"},
        {id: uuidv4(), word: "apply"},
        {id: uuidv4(), word: "basic"},
        {id: uuidv4(), word: "blood"},
        {id: uuidv4(), word: "album"},
        {id: uuidv4(), word: "arena"},
        {id: uuidv4(), word: "basis"},
        {id: uuidv4(), word: "board"},
        {id: uuidv4(), word: "boost"},
        {id: uuidv4(), word: "buyer"},
        {id: uuidv4(), word: "china"},
        {id: uuidv4(), word: "cover"},
        {id: uuidv4(), word: "booth"},
        {id: uuidv4(), word: "cable"},
        {id: uuidv4(), word: "chose"},
        {id: uuidv4(), word: "craft"},
        {id: uuidv4(), word: "bound"},
        {id: uuidv4(), word: "calif"},
        {id: uuidv4(), word: "civil"},
        {id: uuidv4(), word: "crash"},
        {id: uuidv4(), word: "brain"},
        {id: uuidv4(), word: "carry"},
        {id: uuidv4(), word: "claim"},
        {id: uuidv4(), word: "cream"},
        {id: uuidv4(), word: "brand"},
        {id: uuidv4(), word: "catch"},
        {id: uuidv4(), word: "class"},
        {id: uuidv4(), word: "crime"},
        {id: uuidv4(), word: "bread"},
        {id: uuidv4(), word: "cause"},
        {id: uuidv4(), word: "clean"},
        {id: uuidv4(), word: "cross"},
        {id: uuidv4(), word: "break"},
        {id: uuidv4(), word: "chain"},
        {id: uuidv4(), word: "clear"},
        {id: uuidv4(), word: "crowd"},
        {id: uuidv4(), word: "breed"},
        {id: uuidv4(), word: "chair"},
        {id: uuidv4(), word: "click"},
        {id: uuidv4(), word: "crown"},
        {id: uuidv4(), word: "brief"},
        {id: uuidv4(), word: "chart"},
        {id: uuidv4(), word: "clock"},
        {id: uuidv4(), word: "curve"},
        {id: uuidv4(), word: "bring"},
        {id: uuidv4(), word: "chase"},
        {id: uuidv4(), word: "close"},
        {id: uuidv4(), word: "cycle"},
        {id: uuidv4(), word: "broad"},
        {id: uuidv4(), word: "cheap"},
        {id: uuidv4(), word: "coach"},
        {id: uuidv4(), word: "daily"},
        {id: uuidv4(), word: "broke"},
        {id: uuidv4(), word: "check"},
        {id: uuidv4(), word: "coast"},
        {id: uuidv4(), word: "dance"},
        {id: uuidv4(), word: "brown"},
        {id: uuidv4(), word: "chest"},
        {id: uuidv4(), word: "could"},
        {id: uuidv4(), word: "dated"},
        {id: uuidv4(), word: "build"},
        {id: uuidv4(), word: "chief"},
        {id: uuidv4(), word: "count"},
        {id: uuidv4(), word: "dealt"},
        {id: uuidv4(), word: "built"},
        {id: uuidv4(), word: "child"},
        {id: uuidv4(), word: "court"},
        {id: uuidv4(), word: "death"},
        {id: uuidv4(), word: "debut"},
        {id: uuidv4(), word: "entry"},
        {id: uuidv4(), word: "forth"},
        {id: uuidv4(), word: "group"},
        {id: uuidv4(), word: "delay"},
        {id: uuidv4(), word: "equal"},
        {id: uuidv4(), word: "forty"},
        {id: uuidv4(), word: "grown"},
        {id: uuidv4(), word: "depth"},
        {id: uuidv4(), word: "error"},
        {id: uuidv4(), word: "forum"},
        {id: uuidv4(), word: "guard"},
        {id: uuidv4(), word: "doing"},
        {id: uuidv4(), word: "event"},
        {id: uuidv4(), word: "found"},
        {id: uuidv4(), word: "guess"},
        {id: uuidv4(), word: "doubt"},
        {id: uuidv4(), word: "every"},
        {id: uuidv4(), word: "frame"},
        {id: uuidv4(), word: "guest"},
        {id: uuidv4(), word: "dozen"},
        {id: uuidv4(), word: "exact"},
        {id: uuidv4(), word: "frank"},
        {id: uuidv4(), word: "guide"},
        {id: uuidv4(), word: "draft"},
        {id: uuidv4(), word: "exist"},
        {id: uuidv4(), word: "fraud"},
        {id: uuidv4(), word: "happy"},
        {id: uuidv4(), word: "drama"},
        {id: uuidv4(), word: "extra"},
        {id: uuidv4(), word: "fresh"},
        {id: uuidv4(), word: "harry"},
        {id: uuidv4(), word: "drawn"},
        {id: uuidv4(), word: "faith"},
        {id: uuidv4(), word: "front"},
        {id: uuidv4(), word: "heart"},
        {id: uuidv4(), word: "dream"},
        {id: uuidv4(), word: "false"},
        {id: uuidv4(), word: "fruit"},
        {id: uuidv4(), word: "heavy"},
        {id: uuidv4(), word: "dress"},
        {id: uuidv4(), word: "fault"},
        {id: uuidv4(), word: "fully"},
        {id: uuidv4(), word: "hence"},
        {id: uuidv4(), word: "drill"},
        {id: uuidv4(), word: "fiber"},
        {id: uuidv4(), word: "funny"},
        {id: uuidv4(), word: "night"},
        {id: uuidv4(), word: "drink"},
        {id: uuidv4(), word: "field"},
        {id: uuidv4(), word: "giant"},
        {id: uuidv4(), word: "horse"},
        {id: uuidv4(), word: "drive"},
        {id: uuidv4(), word: "fifth"},
        {id: uuidv4(), word: "given"},
        {id: uuidv4(), word: "hotel"},
        {id: uuidv4(), word: "drove"},
        {id: uuidv4(), word: "fifty"},
        {id: uuidv4(), word: "glass"},
        {id: uuidv4(), word: "house"},
        {id: uuidv4(), word: "dying"},
        {id: uuidv4(), word: "fight"},
        {id: uuidv4(), word: "globe"},
        {id: uuidv4(), word: "human"},
        {id: uuidv4(), word: "eager"},
        {id: uuidv4(), word: "final"},
        {id: uuidv4(), word: "going"},
        {id: uuidv4(), word: "ideal"},
        {id: uuidv4(), word: "early"},
        {id: uuidv4(), word: "first"},
        {id: uuidv4(), word: "grace"},
        {id: uuidv4(), word: "image"},
        {id: uuidv4(), word: "earth"},
        {id: uuidv4(), word: "fixed"},
        {id: uuidv4(), word: "grade"},
        {id: uuidv4(), word: "index"},
        {id: uuidv4(), word: "eight"},
        {id: uuidv4(), word: "flash"},
        {id: uuidv4(), word: "grand"},
        {id: uuidv4(), word: "inner"},
        {id: uuidv4(), word: "elite"},
        {id: uuidv4(), word: "fleet"},
        {id: uuidv4(), word: "grant"},
        {id: uuidv4(), word: "input"},
        {id: uuidv4(), word: "empty"},
        {id: uuidv4(), word: "floor"},
        {id: uuidv4(), word: "grass"},
        {id: uuidv4(), word: "issue"},
        {id: uuidv4(), word: "enemy"},
        {id: uuidv4(), word: "fluid"},
        {id: uuidv4(), word: "great"},
        {id: uuidv4(), word: "irony"},
        {id: uuidv4(), word: "enjoy"},
        {id: uuidv4(), word: "focus"},
        {id: uuidv4(), word: "green"},
        {id: uuidv4(), word: "juice"},
        {id: uuidv4(), word: "enter"},
        {id: uuidv4(), word: "force"},
        {id: uuidv4(), word: "gross"},
        {id: uuidv4(), word: "joint"},
        {id: uuidv4(), word: "judge"},
        {id: uuidv4(), word: "metal"},
        {id: uuidv4(), word: "media"},
        {id: uuidv4(), word: "newly"},
        {id: uuidv4(), word: "known"},
        {id: uuidv4(), word: "local"},
        {id: uuidv4(), word: "might"},
        {id: uuidv4(), word: "noise"},
        {id: uuidv4(), word: "label"},
        {id: uuidv4(), word: "logic"},
        {id: uuidv4(), word: "minor"},
        {id: uuidv4(), word: "north"},
        {id: uuidv4(), word: "large"},
        {id: uuidv4(), word: "loose"},
        {id: uuidv4(), word: "minus"},
        {id: uuidv4(), word: "noted"},
        {id: uuidv4(), word: "laser"},
        {id: uuidv4(), word: "lower"},
        {id: uuidv4(), word: "mixed"},
        {id: uuidv4(), word: "novel"},
        {id: uuidv4(), word: "later"},
        {id: uuidv4(), word: "lucky"},
        {id: uuidv4(), word: "model"},
        {id: uuidv4(), word: "nurse"},
        {id: uuidv4(), word: "laugh"},
        {id: uuidv4(), word: "lunch"},
        {id: uuidv4(), word: "money"},
        {id: uuidv4(), word: "occur"},
        {id: uuidv4(), word: "layer"},
        {id: uuidv4(), word: "lying"},
        {id: uuidv4(), word: "month"},
        {id: uuidv4(), word: "ocean"},
        {id: uuidv4(), word: "learn"},
        {id: uuidv4(), word: "magic"},
        {id: uuidv4(), word: "moral"},
        {id: uuidv4(), word: "offer"},
        {id: uuidv4(), word: "lease"},
        {id: uuidv4(), word: "major"},
        {id: uuidv4(), word: "motor"},
        {id: uuidv4(), word: "often"},
        {id: uuidv4(), word: "least"},
        {id: uuidv4(), word: "maker"},
        {id: uuidv4(), word: "mount"},
        {id: uuidv4(), word: "order"},
        {id: uuidv4(), word: "leave"},
        {id: uuidv4(), word: "march"},
        {id: uuidv4(), word: "mouse"},
        {id: uuidv4(), word: "other"},
        {id: uuidv4(), word: "legal"},
        {id: uuidv4(), word: "music"},
        {id: uuidv4(), word: "mouth"},
        {id: uuidv4(), word: "ought"},
        {id: uuidv4(), word: "level"},
        {id: uuidv4(), word: "match"},
        {id: uuidv4(), word: "movie"},
        {id: uuidv4(), word: "paint"},
        {id: uuidv4(), word: "light"},
        {id: uuidv4(), word: "mayor"},
        {id: uuidv4(), word: "needs"},
        {id: uuidv4(), word: "paper"},
        {id: uuidv4(), word: "limit"},
        {id: uuidv4(), word: "meant"},
        {id: uuidv4(), word: "never"},
        {id: uuidv4(), word: "party"},
        {id: uuidv4(), word: "peace"},
        {id: uuidv4(), word: "power"},
        {id: uuidv4(), word: "radio"},
        {id: uuidv4(), word: "round"},
        {id: uuidv4(), word: "panel"},
        {id: uuidv4(), word: "press"},
        {id: uuidv4(), word: "raise"},
        {id: uuidv4(), word: "route"},
        {id: uuidv4(), word: "phase"},
        {id: uuidv4(), word: "price"},
        {id: uuidv4(), word: "range"},
        {id: uuidv4(), word: "royal"},
        {id: uuidv4(), word: "phone"},
        {id: uuidv4(), word: "pride"},
        {id: uuidv4(), word: "rapid"},
        {id: uuidv4(), word: "rural"},
        {id: uuidv4(), word: "photo"},
        {id: uuidv4(), word: "prime"},
        {id: uuidv4(), word: "ratio"},
        {id: uuidv4(), word: "scale"},
        {id: uuidv4(), word: "piece"},
        {id: uuidv4(), word: "print"},
        {id: uuidv4(), word: "reach"},
        {id: uuidv4(), word: "scene"},
        {id: uuidv4(), word: "pilot"},
        {id: uuidv4(), word: "prior"},
        {id: uuidv4(), word: "ready"},
        {id: uuidv4(), word: "scope"},
        {id: uuidv4(), word: "pitch"},
        {id: uuidv4(), word: "prize"},
        {id: uuidv4(), word: "refer"},
        {id: uuidv4(), word: "score"},
        {id: uuidv4(), word: "place"},
        {id: uuidv4(), word: "proof"},
        {id: uuidv4(), word: "right"},
        {id: uuidv4(), word: "sense"},
        {id: uuidv4(), word: "plain"},
        {id: uuidv4(), word: "proud"},
        {id: uuidv4(), word: "rival"},
        {id: uuidv4(), word: "serve"},
        {id: uuidv4(), word: "plane"},
        {id: uuidv4(), word: "prove"},
        {id: uuidv4(), word: "river"},
        {id: uuidv4(), word: "seven"},
        {id: uuidv4(), word: "plant"},
        {id: uuidv4(), word: "queen"},
        {id: uuidv4(), word: "quick"},
        {id: uuidv4(), word: "shall"},
        {id: uuidv4(), word: "plate"},
        {id: uuidv4(), word: "sixth"},
        {id: uuidv4(), word: "stand"},
        {id: uuidv4(), word: "shape"},
        {id: uuidv4(), word: "point"},
        {id: uuidv4(), word: "quiet"},
        {id: uuidv4(), word: "roman"},
        {id: uuidv4(), word: "share"},
        {id: uuidv4(), word: "pound"},
        {id: uuidv4(), word: "quite"},
        {id: uuidv4(), word: "rough"},
        {id: uuidv4(), word: "sharp"},
        {id: uuidv4(), word: "sheet"},
        {id: uuidv4(), word: "spare"},
        {id: uuidv4(), word: "style"},
        {id: uuidv4(), word: "times"},
        {id: uuidv4(), word: "shelf"},
        {id: uuidv4(), word: "speak"},
        {id: uuidv4(), word: "sugar"},
        {id: uuidv4(), word: "tired"},
        {id: uuidv4(), word: "shell"},
        {id: uuidv4(), word: "speed"},
        {id: uuidv4(), word: "suite"},
        {id: uuidv4(), word: "title"},
        {id: uuidv4(), word: "shift"},
        {id: uuidv4(), word: "spend"},
        {id: uuidv4(), word: "super"},
        {id: uuidv4(), word: "today"},
        {id: uuidv4(), word: "shirt"},
        {id: uuidv4(), word: "spent"},
        {id: uuidv4(), word: "sweet"},
        {id: uuidv4(), word: "topic"},
        {id: uuidv4(), word: "shock"},
        {id: uuidv4(), word: "split"},
        {id: uuidv4(), word: "table"},
        {id: uuidv4(), word: "total"},
        {id: uuidv4(), word: "shoot"},
        {id: uuidv4(), word: "spoke"},
        {id: uuidv4(), word: "taken"},
        {id: uuidv4(), word: "touch"},
        {id: uuidv4(), word: "short"},
        {id: uuidv4(), word: "sport"},
        {id: uuidv4(), word: "taste"},
        {id: uuidv4(), word: "tough"},
        {id: uuidv4(), word: "shown"},
        {id: uuidv4(), word: "staff"},
        {id: uuidv4(), word: "taxes"},
        {id: uuidv4(), word: "tower"},
        {id: uuidv4(), word: "sight"},
        {id: uuidv4(), word: "stage"},
        {id: uuidv4(), word: "teach"},
        {id: uuidv4(), word: "track"},
        {id: uuidv4(), word: "since"},
        {id: uuidv4(), word: "stake"},
        {id: uuidv4(), word: "teeth"},
        {id: uuidv4(), word: "trade"},
        {id: uuidv4(), word: "sixty"},
        {id: uuidv4(), word: "start"},
        {id: uuidv4(), word: "texas"},
        {id: uuidv4(), word: "treat"},
        {id: uuidv4(), word: "sized"},
        {id: uuidv4(), word: "state"},
        {id: uuidv4(), word: "thank"},
        {id: uuidv4(), word: "trend"},
        {id: uuidv4(), word: "skill"},
        {id: uuidv4(), word: "steam"},
        {id: uuidv4(), word: "theft"},
        {id: uuidv4(), word: "trial"},
        {id: uuidv4(), word: "sleep"},
        {id: uuidv4(), word: "steel"},
        {id: uuidv4(), word: "their"},
        {id: uuidv4(), word: "tried"},
        {id: uuidv4(), word: "slide"},
        {id: uuidv4(), word: "stick"},
        {id: uuidv4(), word: "theme"},
        {id: uuidv4(), word: "tries"},
        {id: uuidv4(), word: "small"},
        {id: uuidv4(), word: "still"},
        {id: uuidv4(), word: "there"},
        {id: uuidv4(), word: "truck"},
        {id: uuidv4(), word: "smart"},
        {id: uuidv4(), word: "stock"},
        {id: uuidv4(), word: "these"},
        {id: uuidv4(), word: "truly"},
        {id: uuidv4(), word: "smile"},
        {id: uuidv4(), word: "stone"},
        {id: uuidv4(), word: "thick"},
        {id: uuidv4(), word: "trust"},
        {id: uuidv4(), word: "smith"},
        {id: uuidv4(), word: "stood"},
        {id: uuidv4(), word: "thing"},
        {id: uuidv4(), word: "truth"},
        {id: uuidv4(), word: "smoke"},
        {id: uuidv4(), word: "store"},
        {id: uuidv4(), word: "think"},
        {id: uuidv4(), word: "twice"},
        {id: uuidv4(), word: "solid"},
        {id: uuidv4(), word: "storm"},
        {id: uuidv4(), word: "third"},
        {id: uuidv4(), word: "under"},
        {id: uuidv4(), word: "solve"},
        {id: uuidv4(), word: "story"},
        {id: uuidv4(), word: "those"},
        {id: uuidv4(), word: "undue"},
        {id: uuidv4(), word: "sorry"},
        {id: uuidv4(), word: "strip"},
        {id: uuidv4(), word: "three"},
        {id: uuidv4(), word: "union"},
        {id: uuidv4(), word: "sound"},
        {id: uuidv4(), word: "stuck"},
        {id: uuidv4(), word: "threw"},
        {id: uuidv4(), word: "unity"},
        {id: uuidv4(), word: "south"},
        {id: uuidv4(), word: "study"},
        {id: uuidv4(), word: "throw"},
        {id: uuidv4(), word: "until"},
        {id: uuidv4(), word: "space"},
        {id: uuidv4(), word: "stuff"},
        {id: uuidv4(), word: "tight"},
        {id: uuidv4(), word: "upper"},
        {id: uuidv4(), word: "upset"},
        {id: uuidv4(), word: "whole"},
        {id: uuidv4(), word: "waste"},
        {id: uuidv4(), word: "wound"},
        {id: uuidv4(), word: "urban"},
        {id: uuidv4(), word: "whose"},
        {id: uuidv4(), word: "watch"},
        {id: uuidv4(), word: "write"},
        {id: uuidv4(), word: "usage"},
        {id: uuidv4(), word: "woman"},
        {id: uuidv4(), word: "water"},
        {id: uuidv4(), word: "wrong"},
        {id: uuidv4(), word: "usual"},
        {id: uuidv4(), word: "train"},
        {id: uuidv4(), word: "wheel"},
        {id: uuidv4(), word: "wrote"},
        {id: uuidv4(), word: "valid"},
        {id: uuidv4(), word: "world"},
        {id: uuidv4(), word: "where"},
        {id: uuidv4(), word: "yield"},
        {id: uuidv4(), word: "value"},
        {id: uuidv4(), word: "worry"},
        {id: uuidv4(), word: "which"},
        {id: uuidv4(), word: "young"},
        {id: uuidv4(), word: "video"},
        {id: uuidv4(), word: "worse"},
        {id: uuidv4(), word: "while"},
        {id: uuidv4(), word: "youth"},
        {id: uuidv4(), word: "virus"},
        {id: uuidv4(), word: "worst"},
        {id: uuidv4(), word: "white"},
        {id: uuidv4(), word: "worth"},
        {id: uuidv4(), word: "visit"},
        {id: uuidv4(), word: "would"},
        {id: uuidv4(), word: "vital"},
        {id: uuidv4(), word: "voice"},
	];
	let correctWord: {id: number, word: string} = words[Math.floor(Math.random() * words.length)];

    let turn: number = 0;
    let isCorrect: boolean = false;
    let gameOver = false;
    let currentGuess: string = "";
    let guesses: {letter: string, color: string}[][] = [
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
    let history: string[] = [];
    let modalOpen: boolean = false;
    let modalTitle: string = "";
    let modalContent: string = "";

    const toggleModal = () => {
        modalOpen = !modalOpen;
    };

    const addGuess = (formattedGuess) => {
        modalTitle = "";
        modalContent = "";
        isCorrect = false;

        guesses[turn] = formattedGuess;
        history = [...history, currentGuess];

        turn += 1;
        if (turn == 6 && currentGuess != correctWord.word) {
            modalTitle = "You Lost :(";
            modalContent = `
                <p><strong>You Lost</strong>, the word was <strong>${correctWord.word}</strong>.</p>
                <p>It's okay! You can always go again!</p>
            `;
            toggleModal();
            gameOver = true;
        }

        if (currentGuess == correctWord.word) {
            isCorrect = true;
            modalTitle = "Victory";
            modalContent = `
                <p><strong>You Win!</strong> The word was <strong>${correctWord.word}</strong>!</p>
                <p>You guessed <strong>${correctWord.word}</strong> in <strong>${turn}</strong> tries</p>
            `;
            toggleModal();
            gameOver = true;
        }

        currentGuess = "";
    };

	const formatGuess = () => {
        let correctWordArray = [...correctWord.word];
        let formattedGuess: {letter: string, color: string}[] = [...currentGuess].map((letter) => {
            return {letter: letter, color: "gray"}
        });

        formattedGuess.forEach((letter, index) => {
            if (correctWordArray[index] == letter.letter) {
                formattedGuess[index].color = "green";
                correctWord[index] = null;
            }
            else if (correctWordArray.includes(letter.letter) && letter.color != "green") {
                formattedGuess[index].color = "yellow";
                correctWordArray[correctWordArray.indexOf(letter.letter)] = null;
            }
        });
        return formattedGuess;
    };

    const handleInput = (key) => {
        modalTitle = "";
        modalContent = "";

        if (key.detail != 0) {
            key = key.detail.key;
        }
        else {
            key = key.key;
        }

        if (key == "Backspace") {
            if (currentGuess.length > 0) {
                currentGuess = currentGuess.slice(0, -1);
            }
        }
        if (key == "Enter") {
            if (currentGuess.length == 5) {
                if (turn != 6) {
                    if (!history.includes(currentGuess)) {
                        let formattedGuess: {letter: string, color: string}[] = formatGuess();
                        addGuess(formattedGuess);
                    }
                }
            }
            else {
                modalTitle = "Alert";
                modalContent = `
                    <p>Your word is too short. A word must be 5 letters long.</p>
                `;
                toggleModal();
            }
        }
        else if (/^[A-Za-z]$/.test(key)) {
            if (currentGuess.length < 5) {
                currentGuess += key.toLowerCase();
            }
        }
    };

    const restartGame = () => {
        correctWord = words[Math.floor(Math.random() * words.length)];

        turn = 0;
        isCorrect = false;
        gameOver = false;
        currentGuess = "";
        guesses = [
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
        history = [];
        modalOpen = false;
        modalTitle = "";
        modalContent = "";
        console.log("The answer is: " + correctWord.word + " :)");
    };

    window.addEventListener("keyup", handleInput);

    modalTitle = "How to Play";
    modalContent = `
        <h1>How to Play</h1>
        <p>Guess the Wordle in 6 tries.</p>
        <p>Each guess must be a valid 5-letter word.</p>
        <p>The color of the tiles will change to show how close your guess was to the word.</p>
        <strong>Examples</strong>
        <div class="row">
            <div style="background-color: #6aaa64; color: white;">W</div><div>E</div><div>A</div><div>R</div><div>Y</div>
        </div>
        <p><strong>W</strong> is in the word and in the correct spot.<p>
        <div class="row">
            <div style="background-color: #f7da21; color: white;">I</div><div>M</div><div>A</div><div>G</div><div>E</div>
        </div>
        <p><strong>I</strong> is in the word but in the wrong spot.<p>
        <div class="row">
            <div style="background-color: #86888a; color: white;">U</div><div>N</div><div>D</div><div>E</div><div>R</div>
        </div>
        <p><strong>U</strong> is not in the word in any spot..<p>
    `  
    toggleModal();
</script>

<main>
    <Modal {modalOpen} on:toggleModal={toggleModal}>
        <div id="modal-header">
            <div id="modal-title">{modalTitle}</div>
            <div id="modal-close" on:click={toggleModal}>&times;</div>
        </div>
        <div id="modal-content">
            {@html modalContent}
        </div>
        <div id="modal-footer">
            <button on:click={toggleModal}>Ok</button>
            { #if gameOver}
                <button on:click={restartGame}>Try Again</button>
            { /if }
        </div>
    </Modal>
    <div id="header">
        <h1>Wordle</h1>
        <p>Created By: <strong>NoobBit</strong></p>
    </div>
	<Game {correctWord} {turn} {isCorrect} {gameOver} {currentGuess} {guesses} {history} on:formatGuess={formatGuess} on:addGuess={addGuess}/>
	<!-- <button on:click={() => correctWord = words[Math.floor(Math.random() * words.length)]}>Re-Generate</button> -->
    <Keyboard on:handleInput={handleInput}/>
</main>