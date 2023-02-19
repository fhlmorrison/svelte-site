<script lang="ts">
  import RobotViewer from "./lib/RobotViewer/RobotViewer.svelte";
  import Social from "./lib/Social.svelte";
  import NameLogo from "./lib/NameLogo.svelte";
  import FaGithub from "svelte-icons/fa/FaGithub.svelte";
  import FaLinkedin from "svelte-icons/fa/FaLinkedin.svelte";
</script>

<div class="header">
  <NameLogo size="2.5" />
</div>
<main>
  <RobotViewer />
  <div>
    <a href="/" target="_self">
      <img src="/FM.svg" class="logo" alt="FM Logo" />
    </a>
  </div>
  <h1>Big text</h1>

  <div class="card">card placeholder</div>

  <p>Check out ____</p>

  <p class="read-the-docs">Light text placeholder</p>

  <Social href="https://github.com/fhlmorrison" text="fhlmorrison">
    <FaGithub />
  </Social>
  <Social
    href="https://www.linkedin.com/in/fhlmorrison/"
    text="Fraser Morrison"
  >
    <FaLinkedin />
  </Social>
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
    display: flex;
    justify-content: center;
  }
</style>
