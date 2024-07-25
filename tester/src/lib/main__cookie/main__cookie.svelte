<script>
  let number = 0;
  const shareData = {
  title: number,
  text: `MY SCORE ${number}`,
  url: "https://chatgpt.com/c/9fc6da7f-a754-4d29-b5f5-f09da05f4a39",
};
let resultText = '';
async function share() {
    try {
      await navigator.share(shareData);
      // resultText = 'MDN shared successfully';
    } catch (err) {
      resultText = `Error: ${err}`;
    }
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
    <button class="buttonC__mainB" on:click={() => number++}></button>
  </div>
  <div class="upgrades">
      
  </div>
</div>

<style>
  .border {
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
    background: url(./pngwing.com.png);
    background-repeat: no-repeat;
    background-size:cover;
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
</style>
