<script>
  import { createEventDispatcher } from "svelte";

  export let imgUrl = null,
    textT,
    textD,
    priceUpgrade = 10,
    number;
  let level = 0;
  const dispatch = createEventDispatcher();
  const priceIncrease = () => {
    if (number >= priceUpgrade) {
      dispatch("increaseClickPower");
      dispatch("deductNumber", priceUpgrade);
      priceUpgrade = Math.round((priceUpgrade *= 1.2));
      console.log(typeof priceUpgrade);
      level++;
    } else {
      alert("🍪 NOT ENOUGH COOKIES! 🍪");
    }
  };
</script>

<div class="upgrades">
  <img src={imgUrl} alt="nothing" />
  <div>
    <h2>{textT}</h2>
    <div>
      <p>{textD}</p>
      <p>level: {level}</p>
    </div>
  </div>
  <button on:click={priceIncrease}>{priceUpgrade}</button>
</div>

<style>
  .upgrades {
    display: flex;
    flex: row;
    justify-content: space-between;
  }
  .upgrades > img {
    border: 1px solid gray;
    border-radius: 1px 3px;
  }
  .upgrades > div > h2 {
    color: antiquewhite;
    font-size: 24px;
  }
  .upgrades > button {
    width: 50px;
  }
  .upgrades > div > div {
    display: flex;
    justify-content: space-between;
  }
  .upgrades > div > div > p {
    color: antiquewhite;
    font-size: 14px;
  }
</style>
