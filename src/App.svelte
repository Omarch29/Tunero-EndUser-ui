<script lang="ts">
  import '@skeletonlabs/skeleton/themes/theme-hamlindigo.css';
  import { Route, Router, Link } from 'svelte-navigator';
  import Home from './pages/Home.svelte';
  import CounterRoute from './pages/CounterRoute.svelte';
</script>

<main>
  <body data-theme="hamlindigo">
    <Router>
    <Route path="/" component={Home}></Route>
    <Route path="/counter" component={CounterRoute}></Route>
    </Router>
  </body>
</main>