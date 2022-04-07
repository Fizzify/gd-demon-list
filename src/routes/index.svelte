<script context="module">
  export async function load({ fetch }) {
    const res = await fetch('https://pointercrate.com//api/v2/demons/listed/?limit=10');
    const data = await res.json();
    if (res.ok) {
      return {
	props: { demon: data }
      }
    }
  }
</script>

<script>
  import Demons from '../components/Demons.svelte';
  export let demon;
</script>

<body>
  <section>
    <Demons {demon} />
  </section>
</body>
<style>
  body {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    font-family: Arial, "Helvetica Neue", sans-serif;
  }
</style>

<svelte:head>
  <title>Pointercrate API Practice</title>
</svelte:head>
