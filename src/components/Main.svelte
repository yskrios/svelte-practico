<script>
  import Sidebar from "./Sidebar.svelte";
</script>

<main class="Main">
  <div class="Main-container">
    <div class="main-content">
      <slot />
      <Sidebar />
    </div>
  </div>
</main>

<style>
  .Main-container {
    display: grid;
    grid-template-columns: minmax(auto, 1024px);
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
