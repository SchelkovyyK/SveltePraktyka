<script>
  import { onMount } from "svelte";

  let coffees = [];
  let loading = true;

  onMount(async () => {
    try {
      const response = await fetch("https://api.sampleapis.com/beers/ale");
      coffees = await response.json();
    } catch (error) {
      console.error("Error fetching coffee data:", error);
    } finally {
      loading = false;
    }
  });
</script>

<ul class="coffee-list">
  {#each coffees as coffee}
    <li class="coffee-item">
      <h2>{coffee.name}</h2>
      <p>{coffee.price}</p>
    </li>
  {/each}
</ul>

<style>
  .coffee-list {
    list-style: none;
    padding: 30px;
    
    display: grid;
    grid-template-columns: repeat(8, 1fr);
    grid-gap:10px
  }
  .coffee-item {
    font-size: 12px;
    background: gray;
    padding: 10px;
  }
</style>
