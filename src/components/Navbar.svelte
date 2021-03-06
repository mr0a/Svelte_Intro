<script>
    import Navlink from './Navlink.svelte'
    export let user = {};

    let current = 'Dashboard';

    function changeCurrent(event){
        current = event.detail.text;
    }
</script>

<div>
    <ul>
        {#if !user.isAuth}
            <Navlink href={'/'} text={'Login'} active={current === 'Login'} on:activate={changeCurrent} />
        {:else}
        <Navlink href={'/'} text={'Dashboard'} active={current === 'Dashboard'} on:activate={changeCurrent}/>
        <Navlink href={'/'} text={'Profile'} active={current === 'Profile'} on:activate={changeCurrent}/>
        <Navlink href={'/'} text={'Logout'} active={current === 'Logout'} on:activate={changeCurrent}/>

        {/if}
    </ul>
</div>

<style>
    div {
        height: 20px;
        padding: 10px 15px;
        background-color: #795283;
    }

    ul {
        padding: 0;
        list-style: none;
        margin: auto 0 auto auto;
    }
</style>
