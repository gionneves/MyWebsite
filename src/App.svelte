<script>
	import { Router, Link, Route } from "svelte-routing";
	import Home from "./routes/Home.svelte";
	import Portfolio from "./routes/Portfolio.svelte";

	export let url = "";
</script>

<Router {url}>
	<nav>
		<Link class="text-padding" to="/">Home</Link>
		<Link class="text-padding" to="Portfolio">Portfólio</Link>
		<Link class="text-padding" to="Videos">Vídeos</Link>
		<Link class="text-padding" to="Downloads">Downloads</Link>
	</nav>
	<div>
		<Route path="Portfolio" component={Portfolio} />
		<Route path="/" component={Home} />
	</div>
</Router>
