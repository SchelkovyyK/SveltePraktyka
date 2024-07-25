<footer class="footer">
  <div class="footer__div">
    <button class="footer__div__button">main</button>
    <button class="footer__div__button">contacts</button>
    <button class="footer__div__button">offers</button>
  </div>
</footer>

<style>
  .footer {
    position: relative;
    background: rgb(69, 89, 95);
    height: 20vh;
  }
  .footer__div {
    position: absolute;
    top: 50%;
    width: 100%;
    transform: translateY(-50%);
    display: flex;
    /* flex-direction:column ; */
    justify-content: space-evenly;
  }
  .footer__div__button {
    padding: 20px 80px;
    background: rgba(99, 107, 107, 0.332);
    border-radius: 5px;
    border: none;
    transition: 1s;
    color: antiqueblack;
  }
  .footer__div__button:hover {
    background: rgb(149, 176, 255);
  }
  .footer__div__button:focus {
    background: rgb(0, 53, 211);
  }
</style>
