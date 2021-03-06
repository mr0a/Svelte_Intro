<script>
  import Navbar from './components/Navbar.svelte';

  let user = {
    isAuth: false
  }
</script>

<Navbar user={user} />