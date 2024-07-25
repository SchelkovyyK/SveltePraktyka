<script>
  export let color;
  import MainText from "$lib/main__text/main__text.svelte";
  import MainImg from "$lib/mian__img/main__img.svelte";
  import MainCoffee from "$lib/main__coffee/main__coffee.svelte";
  import MainCookie from "../../lib/main__cookie/main__cookie.svelte";
</script>

<main style="background: {color}; transition: 1s">
  <!-- <MainImg></MainImg>
  <MainCoffee></MainCoffee> -->
  <MainCookie></MainCookie>
  <MainText {color}></MainText>
</main>

<style>
  main {
    padding: 30px;
    background: black;
  }
</style>
