<script>
	import { Router, Link, Route } from "svelte-routing";
	import Home from "./routes/Home.svelte";
	import Portfolio from "./routes/Portfolio.svelte";
	import Blog from "./routes/Blog.svelte";

	export let url = "";
</script>

<Router {url}>
	<nav>
		<Link class="text-padding" to="/">Home</Link>
		<Link class="text-padding" to="portfolio">Portfólio</Link>
		<Link class="text-padding" to="blog">Blog</Link>
	</nav>
	<div>
		<Route path="blog" component={Blog} />
		<Route path="portfolio" component={Portfolio} />
		<Route path="/" component={Home} />
	</div>
</Router>
