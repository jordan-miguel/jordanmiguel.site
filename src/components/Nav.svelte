<script>
  export let segment;
</script>

<style>
  nav {
    align-items: flex-end;
    display: flex;
    gap: 30%;
    flex: 1;
    justify-content: center;
  }

  a {
    color: #ffffff;
    text-decoration: none;
    padding: 10px 5px;
    display: block;
    position: relative;
    margin-left: 20px;
  }


  a.selected {
    color:#93b5e3;
  }

  @media (max-width: 500px) {
  nav {
    gap: 0%;
    flex:none;
  }
}
</style>

<nav>
  <a class='{segment === undefined ? "selected" : ""}' href='.'>Jordan Miguel</a>
  <a class='{segment === "about" ? "selected" : ""}' href='about'>About</a>
</nav>
