<script>
    export let imgUrl, textT, textD;
</script>

<div class="upgrades">
  <img src={imgUrl} alt="" />
  <div>
    <h2>{textT}</h2>
    <p>{textD}</p>
  </div>
</div>

<style>
    .upgrades{
        display: flex;
        flex: row;
    }
    .upgrades > img {
        border: 1px solid gray;
        border-radius: 1px 3px ;
    }
    .upgrades > div > h2 {
        color: antiquewhite;
        font-size: 24px;
    }
    .upgrades > div > p {
        color: antiquewhite;
        font-size: 14px;
    }
</style>
