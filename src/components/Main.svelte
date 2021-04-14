<script></script>

<main class="Main">
  <div class="Main-container">
    <div class="main-content">
      <slot />
      <div class="sidebar">sidebar</div>
    </div>
  </div>
</main>

<style>
  .Main-container {
    display: grid;
    grid-template-columns: (auto, 1024px);
    justify-content: center;
    align-items: center;
  }

  .main-content {
    margin: 2em;
    display: grid;
    grid-template-columns: 3fr 1fr;
    gap: 60px;
    justify-content: space-between;
  }
</style>
