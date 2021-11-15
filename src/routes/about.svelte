<script>
  import Bio from '../components/Bio.svelte'
</script>

<style>
  .profile {
    align-items: center;
    display: flex;
    margin-bottom: 50px;
    max-width: 42em;
    margin: 0 auto;
  }

  img {
    width: 100px;
    height: 100px;
    border-radius: 100px;
    display: block;
    margin-right: 20px;
  }

  p {
    font-size: 1.125rem;
  }

  @media (max-width: 500px) {
  .profile {
    margin-bottom: 0;
    flex-direction: column;
    padding: 0 5% 0 5%;
  }
}
</style>

<svelte:head>
  <title>About</title>
</svelte:head>

<div class="profile">
  <img src="https://i.ibb.co/pPfHtPW/side.jpg" alt="Jordan Miguel">
  <p>
    Hi, I'm <strong>Jordan</strong>. I'm a Salesforce developer from London, England.
    You can follow me on <a href="https://twitter.com/jordan__miguel" target="_blank">Twitter</a>,
    see some of my work on <a href="https://github.com/jordan-miguel" target="_blank">GitHub</a>,
    or if you prefer connect on  <a href="https://www.linkedin.com/in/jordanmiguel1/" target="_blank">LinkedIn</a>.
  </p>
</div>
