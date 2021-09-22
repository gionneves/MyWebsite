<script>
	import { Router, Link, Route } from "svelte-routing";
	import Home from "./routes/Home.svelte";
	import Sobre from "./routes/Sobre.svelte";
	import Blog from "./routes/Blog.svelte";

	export let url = "";
</script>

<Router {url}>
	<nav>
		<Link to="/">Home</Link>
		<Link to="Sobre">Sobre</Link>
		<Link to="blog">Blog</Link>
	</nav>
	<div>
		<Route path="blog/:id" component={BlogPost} />
		<Route path="blog" component={Blog} />
		<Route path="Sobre" component={Sobre} />
		<Route path="/"><Home /></Route>
	</div>
</Router>
