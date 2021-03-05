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
    let guitarInput = '';
    let guitars = [];
    let inputElement;

    function addGuitar(){
        // guitars.push(guitarInput);
        // Trigger activity on a variable with assignment
        // guitars = guitars;
        guitars = [...guitars, guitarInput] // Reassigning with new value to trigger update
        guitarInput = ''
        inputElement.focus() // Bring back focus to input after submit
    }
</script>