<script>
  import Card from '../components/Card.svelte';
  let cards = [
    { rank: 'A', suit: 'hearts' },
    { rank: 'K', suit: 'diamonds' },
    { rank: '7', suit: 'clubs' },
  ];
</script>

<main class="flex justify-center items-center h-screen bg-gray-100 space-x-4">
  {#each cards as card}
    <Card rank={card.rank} suit={card.suit} ></Card>
  {/each}
</main>

<style>
  main {
    font-family: sans-serif;
  }
</style>
