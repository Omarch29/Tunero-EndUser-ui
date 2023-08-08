<script lang="ts">
  import svelteLogo from './assets/svelte.svg'
  import viteLogo from '/vite.svg'
  import Counter from './lib/Counter.svelte'

  import { Router, Link, Route } from 'svelte-routing'
  import About from './routes/About.svelte';
  import Home from "./routes/Home.svelte";
  
  import '@skeletonlabs/skeleton/themes/theme-hamlindigo.css';

  import Check from './assets/check.svg'

  export let url = "/";
</script>

<main>
  <body data-theme="hamlindigo">

  <button type="button" class="btn-icon variant-filled">{Check}</button>

  <h1 class="h1-black">Texto centrado sample</h1>
  </body>
  
  <Router {url}>
    <nav>
      <Link to="/">Home</Link>
      <Link to="/about">About</Link>
    </nav>
    <div>
      <Route path="/home" component={Home} />
      <Route path="/about" component={About} />
    </div>
  </Router>
</main>

<style>
  .h1-black {
    color: black;
  }
</style>