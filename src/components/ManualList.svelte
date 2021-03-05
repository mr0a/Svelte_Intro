<form action="">
    <input type="text" bind:value={guitarInput} bind:this={inputElement}>
    <button on:click|preventDefault={addGuitar}>
        Add Guitar
    </button>
</form>

<ul>
    {#each guitars as guitar}
        <li>{guitar}</li>
    {/each}
</ul>

<script>
    import { createEventDispatcher } from 'svelte';
    let dispatch = createEventDispatcher();
    let guitarInput = '';
    let guitars = [];
    let inputElement;

    function addGuitar(){
        // Dispatch a custom event
        dispatch('new-item', {
            value: guitarInput,
        })

        guitars = [...guitars, guitarInput] // Reassigning with new value to trigger update
        
        guitarInput = ''
        inputElement.focus() // Bring back focus to input after submit
    }
</script>