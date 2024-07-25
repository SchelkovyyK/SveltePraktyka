<script>
  import Upgrades from "./upgrades/upgrades.svelte";
  // import herbsBundle from ""
  let number = 0,
    clickPower = 1;

  const shareData = {
    title: number,
    text: `MY SCORE ${number}`,
    url: "https://chatgpt.com/c/9fc6da7f-a754-4d29-b5f5-f09da05f4a39",
  };
  let resultText = "";
  async function share() {
    try {
      await navigator.share(shareData);
      // resultText = 'MDN shared successfully';
    } catch (err) {
      resultText = `Error: ${err}`;
    }
  }
  const clicker = () => {
    number += clickPower;
  };
  const increaseClickPower = () => {
    clickPower++;
  };
  const deductNumber = (event) => {
    const amount = event.detail;
    // console.log(typeof amount, amount)
    number -= amount
    // if(number !== Number){number = 0}
  }
</script>

<div class="border">
  <div class="buttonC">
    <h2>🍪 {number}</h2>
    {#if number}
      <button on:click={share} class="buttonC__nahuiNuzna">share</button>
    {/if}
  </div>
  <div class="cookie">
    <button class="buttonC__mainB" on:click={clicker}></button>
  </div>
  <div class="upgrades">
    <h2>Upgrades:</h2>
    <Upgrades
      imgUrl="null"
      textT="Power of herbs"
      textD="click power +1"
      number={number}
      on:increaseClickPower={increaseClickPower}
      on:deductNumber={deductNumber}
    ></Upgrades>
  </div>
</div>

<style>
  .border {
    overflow: hidden;
    position: relative;
    width: 100%;
    height: 500px;
    margin-bottom: 30px;
    background: rgb(2, 0, 36);
    background: linear-gradient(
      6deg,
      rgba(2, 0, 36, 1) 0%,
      rgba(9, 9, 121, 1) 35%,
      rgba(0, 212, 255, 1) 100%
    );
  }
  .border > h2 {
    text-align: center;
    padding: 20px;
  }
  .cookie {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 300px;
    height: 300px;
    background: url(/images/pngwing.com.png);
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;

    animation: cookies linear infinite 10s;
  }
  @keyframes cookies {
    0% {
      transform: translate(-50%, -50%) rotate(0deg);
    }
    100% {
      transform: translate(-50%, -50%) rotate(360deg);
    }
  }
  .buttonC {

    margin: 0 auto;
    text-align: center;
    padding: 20px;
  }
  .buttonC__mainB {
    cursor: pointer;

    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 80%;
    height: 80%;
    background: rgba(255, 0, 0, 0);
    border-radius: 100%;
    border: none;
    font-size: 30px;
  }
  .buttonC__nahuiNuzna {
    position: absolute;
    bottom: -5px;
    right: -10px;
  }
  .upgrades {
    position: absolute;
    padding: 20px;
    right: 0px;
    width: 500px;
    height: auto;
    background: rgb(108, 35, 0);
    background: linear-gradient(
      0deg,
      rgba(108, 35, 0, 1) 0%,
      rgba(125, 56, 0, 1) 50%,
      rgba(119, 71, 17, 1) 100%
    );
    text-align: center;
    /* transform: translateX(99%); */
    transition: 1s;
  }
  .upgrades:hover {
    /* transform: translateX(0%); */
  }

  .upgrades > h2 {
    font-size: 36px;
    color: rgb(231, 192, 140);
    /* text-decoration: underline rgb(112, 0, 0); */
    padding-bottom: 20px;
  }
</style>
