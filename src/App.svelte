<script>
  import { Router, Link, Route } from 'svelte-routing'
  import Home from './routes/Home.svelte'
  import About from './routes/About.svelte'
  import Blog from './routes/Blog.svelte'

  export let url = '/';
  export let base = '/svelte-routing-demo';
</script>

<Router {url}>
  <nav>
    <Link to={base}>Home</Link>
    <Link to={base + "/about"}>About</Link>
    <Link to={base + "/blog"}>Blog</Link>
  </nav>
  <div>
    <Route path={base + "/blog"} component={Blog} />
    <Route path={base + "/about"} component={About} />
    <Route path={base}><Home /></Route>
  </div>
</Router>