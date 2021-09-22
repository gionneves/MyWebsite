<script>
	import { Router, Link, Route } from "svelte-routing";
	import Home from "./routes/Home.svelte";
	import Sobre from "./routes/Sobre.svelte";

	export let url = "";
</script>

<Router {url}>
	<nav>
		<Link class="text-padding" to="/">Home</Link>
		<Link class="text-padding" to="Sobre">Sobre</Link>
		<Link class="text-padding" to="Videos">Vídeos</Link>
		<Link class="text-padding" to="Downloads">Downloads</Link>
	</nav>
	<div>
		<Route path="Sobre" component={Sobre} />
		<Route path="/" component={Home} />
	</div>
</Router>
