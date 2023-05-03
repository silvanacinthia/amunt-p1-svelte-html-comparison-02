<script>
    import Controls from "./components/Controls.svelte";
    import Result from "./components/Result.svelte";

    let phrase = "Escribe un nombre para comenzar"

    let updatePhrase = (name) => {
        phrase = name.length !== 0 ? `El nombre introducido es ${name} y empieza por ${name.charAt(0)}` : "Escribe un nombre para comenzar";
    };

</script>

<main>
    <Controls onSubmit={updatePhrase}/>
    <Result phrase={phrase} />
</main>

<style>
    main {
        text-align: center;
        padding: 1em;
        max-width: 240px;
        margin: 0 auto;
    }

    @media (min-width: 640px) {
        main {
            max-width: none;
        }
    }
</style>