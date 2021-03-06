<h3>{title}</h3>

<ul>
    {#each items as item}
        <li>{item}</li>
    {/each}
</ul>

<script>
    // Declare props with default value
    export let title = '';
    export let items = [];
</script>
