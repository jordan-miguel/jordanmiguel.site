<script context="module">
  export function preload({ params, query }) {
    return this.fetch(`blog.json`).then(r => r.json()).then(posts => {
      return { posts };
    });
  }
</script>

<script>
  import Bio from '../components/Bio.svelte'
  export let posts;
</script>

<style>

  .post-item {
    margin-bottom: 2rem;
  }

  .post-item a {
    text-decoration: none;
  }

  .post-item h3 {
    color: #93b5e3;
    font-weight: bold;
  }

  .post-item h3:hover {
    background-color: #5175a4;
    transition: all .2s ease-in-out;
  }

  .post-item p {
    margin: 0;
  }

  .post-item-date {
    color: #5175a4;
    text-align: left;
    text-transform:capitalize;
    margin-right: 16px;
  }

  .post-item-footer {
    font-size: 12px;
  }

  .container h1 {
    color: #ffffff;
    margin-bottom: 20px;
  }

  #intro {
    margin-bottom: 50px;
  }

  @media (max-width: 760px) {
  .container {
    margin: 0 auto;
    max-width: 32em;
    width: 100%;
  }
}

@media (max-width: 414px) {
  .container {
    padding: 0 5% 0 5%;
  }

  .container h3 {
    font-size: 16px;
  }
  .container p {
    font-size: 14px;
  }
}

</style>

<svelte:head>
  <title>Jordan Miguel</title>
</svelte:head>

<div class="container">
  <Bio />
  <h1>Blog</h1>
  <p id="intro">A collection of my thoughts on software development, travel, music and all things in between.</p>
  <hr />
  {#each posts as post, index}
  <div class="post-container">
    <div class="post-item">
        <a rel='prefetch' href='blog/{post.slug}'>
          <h3>
            {post.title}
          </h3>
        </a>
      <p>{post.excerpt}</p>
      <div class="post-item-footer">
        <span class="post-item-date"> {post.printDate}</span>
      </div>
    </div>
  </div>
    <hr />
  {/each}
</div>
