<script>
  
  export let color = "black";
  function ChangeColor(arg) {
    if (arg === "red") {
      return (color = "red");
    }
    if (arg === "green") {
      return (color = "green");
    }
    if (arg === "blue") {
      return (color = "blue");
    }
    if (arg === "black") {
      return (color = "black");
    }
  }
</script>

<header class="header">
  <div class="header__div">
    <button
      on:click={() => ChangeColor("red")}
      class="header__div__buttonr header__div__button">main</button
    >
    <button
      on:click={() => ChangeColor("green")}
      class="header__div__buttong header__div__button">contacts</button
    >
    <button
      on:click={() => ChangeColor("blue")}
      class="header__div__buttonb header__div__button">offers</button
    >
    <button
      on:click={() => ChangeColor("black")}
      class="header__div__buttonclear header__div__button">clear</button
    >
    
  </div>
</header>

<style>
  
  .header {
    position: relative;
    background: rgb(179, 243, 245);
    height: 20vh;
  }
  .header__div {
    position: absolute;
    top: 50%;
    width: 100%;
    transform: translateY(-50%);
    display: flex;
    /* flex-direction:column ; */
    justify-content: space-evenly;
  }
  .header__div__button {
    padding: 20px 80px;
    background: rgba(240, 251, 252, 0);
    border-radius: 5px;
    border: none;
    transition: 1s;
  }
  .header__div__buttonr:hover {
    background: rgb(255, 149, 149);
  }
  .header__div__buttonr:focus {
    background: rgb(211, 0, 0);
  }
  .header__div__buttong:hover {
    background: rgb(149, 255, 149);
  }
  .header__div__buttong:focus {
    background: rgb(0, 211, 0);
  }
  .header__div__buttonb:hover {
    background: rgb(149, 176, 255);
  }
  .header__div__buttonb:focus {
    background: rgb(0, 53, 211);
  }
  .header__div__buttonclear:hover {
    background: rgb(43, 43, 43);
  }
  .header__div__buttonclear:focus {
    background: rgb(22, 22, 22);
  }
</style>
