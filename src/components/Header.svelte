<script>
  import Nav from './Nav.svelte'

  export let segment
</script>

<style>
  header {
    display: flex;
    margin: 0 auto;
    width: 100%;
  }
</style>

<header>
  <Nav {segment} />
</header>
