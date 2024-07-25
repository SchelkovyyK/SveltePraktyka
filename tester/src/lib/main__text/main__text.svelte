<script>
  export let color;
</script>

<div class="main__div">
  <!-- block start -->
  <div class="main__div__content">
    <h2>Name of store</h2>
    <p style="color: {color}; transition: 1s">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin
      pellentesque non erat vel eleifend. Nunc vehicula ornare metus, et
      convallis erat. Quisque quis ultricies est. Fusce interdum nunc ex,
      ultricies maximus diam porttitor eget. Ut laoreet pharetra blandit. Nunc
      condimentum mauris ut arcu consequat varius. Nullam non erat in arcu
      accumsan bibendum et in sem. In vulputate lectus non purus consequat
      tincidunt. Vestibulum tortor justo, lacinia efficitur tincidunt ut,
      laoreet quis lorem. Fusce consectetur hendrerit nulla, nec dictum tortor
      pulvinar ac. Cras sit amet maximus enim. Etiam ut ligula faucibus,
      volutpat leo vitae, consequat mi. Phasellus sagittis elit quis lorem
      imperdiet fringilla. Ut faucibus accumsan justo. Proin quis orci
      porttitor, hendrerit nibh finibus, iaculis risus. Praesent diam risus,
      ultrices a ligula sit amet, fermentum consectetur enim. Ut eget quam
      pretium, ultricies sapien sit amet, maximus lorem. Phasellus blandit magna
      non metus venenatis ultricies. Sed ligula nibh, varius eu neque sed,
      mollis ornare turpis. Donec turpis arcu, commodo et nulla in, venenatis
      efficitur magna. Sed posuere sapien id est mattis, consectetur congue
      lectus rhoncus. Fusce vitae viverra ipsum, sed ultricies est. Etiam
      maximus condimentum arcu, id venenatis ex feugiat non. Maecenas ac mattis
      magna. Mauris ante ligula, convallis sit amet nunc accumsan, aliquam
      cursus ligula. Quisque ornare sem diam, sed malesuada libero tristique id.
      Pellentesque habitant morbi tristique senectus et netus et malesuada fames
      ac turpis egestas. Donec eu quam non diam finibus mollis. Nam sollicitudin
      tincidunt tempor. Pellentesque habitant morbi tristique senectus et netus
      et malesuada fames ac turpis egestas. Cras dictum non lorem et lacinia. In
      fermentum tincidunt efficitur. Nulla placerat egestas venenatis.
      Suspendisse magna ex, mollis a faucibus nec, rutrum sed ante. Suspendisse
      ac metus eu ex dapibus tristique. Aenean pharetra, mauris et blandit
      dictum, lacus libero sollicitudin lacus, vel tempus metus nulla non magna.
      Vivamus ullamcorper, nisi eu tempor blandit, urna ligula placerat turpis,
      vitae hendrerit urna leo quis erat. Quisque lorem nibh, venenatis eu
      turpis sed, elementum aliquet nisi. Donec aliquet erat eget pretium
      congue. Etiam aliquam sed velit in lacinia. In euismod elementum leo, vel
      facilisis ante accumsan at. Sed id est enim. Sed sit amet diam ac tortor
      porta auctor quis at velit. Fusce interdum leo sit amet nisl ultrices
      eleifend. Praesent in porta nisl. Aliquam sed leo lacinia, ornare quam
      vitae, fermentum eros. Cras maximus ultrices suscipit. Duis quam lacus,
      vestibulum ut dui eu, egestas porttitor arcu. Proin lacinia in nibh at
      ornare. Nulla facilisi. Nam sit amet justo elementum, vehicula nunc eget,
      feugiat ipsum. Sed nulla neque, semper imperdiet lacinia eu, auctor at
      lorem. Nullam facilisis ante a risus rutrum volutpat. Nam semper ex at
      tortor congue ullamcorper. Curabitur diam neque, efficitur vel ultrices
      vel, placerat ac quam. Nunc turpis est, accumsan a maximus a, tempor ac
      nisi. Interdum et malesuada fames ac ante ipsum primis in faucibus. Donec
      fringilla orci id urna viverra vehicula.
    </p>
  </div>
  <!-- img start -->
  <img
    class="main__div__img"
    src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT3VHslYacveK32f1VX21u2PtG0VjLDth3r6Q&s"
    alt=""
  />
</div>

<style>
  .main__div {
    border: 1px solid black;
    padding: 10px;
    display: flex;
    background: rgb(212, 212, 212);
    height: 90%;
  }
  .main__div__content > p {
    overflow-y: scroll;
    height: 85%;
  }
  .main__div__img {
  }
</style>
