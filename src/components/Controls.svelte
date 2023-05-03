<script>
    export let onSubmit = () => {}
    let name = ""
</script>

<input id="name-input" placeholder="Introduce un nombre" bind:value={name}/>
<button id="submit-button" on:click={() => onSubmit(name)}>Add</button>
