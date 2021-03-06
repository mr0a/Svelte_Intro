

<li><a href="{href}" 
    class:active 
    on:click|preventDefault={handleClick}
    >{text}</a></li>


<style>
li{
    display: inline-block;
    margin: 0;
    padding-left: 15px;
}
a{
    color: white;
}

.active{
    font-weight: bold;
}
</style>

<script>
    export let href='#';
    export let text = 'Dashboard';
    export let active = false;
    import { createEventDispatcher } from 'svelte';

    let dispatch = createEventDispatcher();
    

    function handleClick(){
        dispatch('activate', {
            text: text
        })
    }
</script>