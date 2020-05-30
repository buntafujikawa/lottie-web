<script>

  export let name;

  import lottie from "lottie-web";
  import { onMount } from "svelte"

  onMount(() => {
    const loading = lottie.loadAnimation({
      name: 'loading',
      container: document.getElementById('loading'),
      renderer: 'svg',
      loop: true,
      autoplay: true,
      path: './animations/22189-progress.json'
    });
  });

  function like() {
    lottie.loadAnimation({
      name: 'like',
      container: document.getElementById('like'),
      renderer: 'svg',
      loop: false,
      autoplay: true,
      path: './animations/899-like.json'
    });
  }
</script>

<main>
  <h1>Hello {name}!</h1>
  <div id="loading"></div>

  <div id="like"></div>
  <button on:click="{like}">Like</button>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }
</style>
