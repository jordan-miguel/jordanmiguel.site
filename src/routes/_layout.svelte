<script>
  import Header from '../components/Header.svelte';

  export let segment;
</script>

<style>
  .layout {
    display: flex;
    flex-direction: column;
    min-height: 100%;
    min-height: 100vh;
  }

  main {
    flex: 1;
    margin: 0 auto;
    margin-top:50px;
    box-sizing: border-box;
    width: 100%;
    display: flex;
    flex-direction: column;
  }

  footer {
    color: #AAA;
    font-size: 1em;
    margin: 1em auto;
    max-width: 1400px;
    padding: 1em 2em;
    text-align: center;
    width: 100%;
  }
</style>

<div class="layout">
  <Header {segment}/>

  <main>
    <slot></slot>
  </main>

  <footer>
    <span>
      &copy; {new Date().getFullYear()} Jordan Miguel.<br>
      Powered by <a href="https://svelte.dev/" target="_blank">SvelteKit</a>. Deployed by <a href="https://www.netlify.com/" target="_blank">Netifly</a>.
    </span>
  </footer>
</div>
