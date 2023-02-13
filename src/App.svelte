<script lang="ts">
  import Counter from "./lib/Counter.svelte";
  import NameLogo from "./lib/NameLogo.svelte";
</script>

<div class="header">
  <NameLogo size=2.5/>
</div>
<main>
  <div>
    <a href="/" target="_self">
      <img src="/FM.svg" class="logo" alt="FM Logo" />
    </a>
  </div>
  <h1>Vite + Svelte</h1>

  <div class="card">
    <Counter />
  </div>

  <p>
    Check out <a
      href="https://github.com/sveltejs/kit#readme"
      target="_blank"
      rel="noreferrer">SvelteKit</a
    >, the official Svelte app framework powered by Vite!
  </p>

  <p class="read-the-docs">Click on the Vite and Svelte logos to learn more</p>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .read-the-docs {
    color: #888;
  }
  .header {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
  }
</style>
