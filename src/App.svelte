<script>
  import Navbar from './components/Navbar.svelte';

  let user = {
    isAuth: true
  }
</script>

<Navbar user={user} />