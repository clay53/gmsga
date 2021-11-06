<script lang="ts">
	import { Router, Route } from "svelte-routing";
	import NavItem from "./components/NavItem.svelte";
	import NotFound from "./routes/NotFound.svelte";
	import Home from "./routes/Home.svelte";
	import Events from "./routes/Events.svelte";
	import PowderPuff from "./routes/PowderPuff.svelte";
	import WreathsAcrossAmerica from "./routes/WreathsAcrossAmerica.svelte";
	import MiniThon from "./routes/MiniThon.svelte";

	export let url = "";
</script>

<main>
	<Router url="{url}">
		<nav>
			<NavItem to="/">Home</NavItem>
			<NavItem to="/events">Events</NavItem>
		</nav>
		<div id="page">
			<Route path="/"><Home/></Route>
			<Route path="/events"><Events/></Route>
			<Route path="/powder-puff" let:params>
				<PowderPuff year="{params.year}"/>
			</Route>
			<Route path="/wreaths-across-america" let:params>
				<WreathsAcrossAmerica year="{params.year}"/>
			</Route>
			<Route path="/mini-thon" let:params>
				<MiniThon year="{params.year}"/>
			</Route>
			<Route><NotFound/></Route>
		</div>
		<footer>
			<hr/>
			<a href="https://www.governormifflinsd.org/">Official District Website</a>
			<br>This website is open source: <a href="https://github.com/clay53/gmsga">contribute!</a>
			<p>
				Please aknowledge that this website is developed and maintained by students of Governor Mifflin High School Student Government and is not necessarily reflective of the whole of Governor Mifflin Student Government or the greater Governor Mifflin School District.
			</p>
		</footer>
	</Router>
</main>

<style>
	main {
		text-align: center;
	}

	#page {
		padding: 0 1em 0 1em;
	}

	nav {
		background-color: #FDB414;
		padding: 1em 0;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>