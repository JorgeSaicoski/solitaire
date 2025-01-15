<script>
  export let rank = ''; // Card rank (e.g., 'A', '2', '3', ..., 'K')
  export let suit = ''; // Card suit (e.g., 'hearts', 'diamonds', 'clubs', 'spades')
  export let isFaceDown = true; // Whether the card is face-up or face-down
  function flipCard() {
    isFaceDown = !isFaceDown;
  }
</script>

<button
    onclick={()=>flipCard()}
  class="w-20 h-32 border rounded-lg flex justify-center items-center bg-white shadow-lg transition-all duration-300 ease-in-out"
  class:flip={isFaceDown} 
  class:bg-gray-200={!isFaceDown}
  class:border-gray-700={!isFaceDown}
>
  {#if isFaceDown}
    <div class="bg-blue-500 w-full h-full rounded-lg"></div>
  {:else}   
    <div class="text-xl font-bold">
        <span>{rank}</span>
        <span class="block text-xs">{suit}</span>
      </div>
  {/if}
</button>

<style>
  .flip {
    transform: rotateY(180deg);
  }
</style>
