<footer class="Footer">
  <div class="footer-container">
    <div class="footer-content">
      <div class="footer-copy">❤</div>
      <div class="footer-svelte">
        Proudly powered by svelte
        <img src="svelte.png" alt="logo de svelte" />
      </div>
    </div>
  </div>
</footer>

<style>
  .Footer {
    background-color: rgba(28, 41, 56, 0.8);
    color: #fff;
    padding: 1.5em 0;
    margin: 2em 0 0 0;
    font-size: 13px;
    font-weight: 300;
  }

  .footer-container {
    display: grid;
    grid-template-columns: minmax(auto, 1024px);
    justify-content: center;
    align-items: center;
  }

  .footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .footer-svelte {
    display: flex;
    align-self: center;
  }

  .footer-svelte img {
    margin: 0 0 0 0.5em;
  }
</style>
