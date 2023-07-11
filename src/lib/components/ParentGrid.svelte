<script lang="ts">
  import SubGrid from './SubGrid.svelte';

  const cardData = [
    {
      title: 'Card 1',
      description: 'This is a card description'
    },
    {
      title: 'Card 2',
      description: 'This is a card description'
    },
    {
      title: 'Card 3',
      description: 'This is a card description'
    }
  ];
</script>

<div class="wrapper">
  {#each cardData as card}
    <SubGrid data={card} />
  {/each}
</div>

<style>
  .wrapper {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 1rem;
  }
</style>
