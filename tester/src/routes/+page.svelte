<script>
  import Header from "./header/header.svelte";
  import Main from "./main/main.svelte";
  import Footer from "../footer/footer.svelte";
  let color = "black";
</script>

<Header bind:color></Header>
<Main {color}></Main>

<Footer></Footer>

<style>
</style>
