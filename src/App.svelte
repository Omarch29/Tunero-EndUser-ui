<script lang="ts">
  import { Router, Link, Route } from 'svelte-routing'
  import About from './routes/About.svelte';
  import Home from "./routes/Home.svelte";
  
  import '@skeletonlabs/skeleton/themes/theme-crimson.css';
  import '@skeletonlabs/skeleton/styles/skeleton.css';
  import './app.postcss';

  import { SlideToggle } from '@skeletonlabs/skeleton';

  let value: boolean = false;

  export let url = "/";
</script>

<main>
  <SlideToggle name="slide" bind:checked={value} />
  <body data-theme="crimson">

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