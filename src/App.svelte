<script>
  import List from './components/List.svelte';
  let title = 'My Life';
  import {onMount} from 'svelte'

  let items = [];

  onMount(async () => {
    let response = await fetch('data.json');
    items = await response.json();
  })
</script>

<!-- Anything inside {} is js expression -->
<List title={title} items={items} />