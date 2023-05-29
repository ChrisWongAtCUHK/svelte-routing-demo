<script>
  import { Router, Link, Route } from 'svelte-routing'
  import Home from './routes/Home.svelte'
  import About from './routes/About.svelte'
  import Blog from './routes/Blog.svelte'

  export let url = '/';
</script>

<Router {url}>
  <nav>
    <Link to="/svelte-routing-demo">Home</Link>
    <Link to="/svelte-routing-demo/about">About</Link>
    <Link to="/svelte-routing-demo/blog">Blog</Link>
  </nav>
  <div>
    <Route path="/svelte-routing-demo/blog" component={Blog} />
    <Route path="/svelte-routing-demo/about" component={About} />
    <Route path="/svelte-routing-demo"><Home /></Route>
  </div>
</Router>