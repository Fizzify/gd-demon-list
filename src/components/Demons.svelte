<script>
  export let demon;
  import DemonCard from './DemonCard.svelte';
</script>

<div class="demon-list">
  {#each demon as level}
    <DemonCard {level} />
  {/each}
</div>
