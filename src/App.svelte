<script>
	export const url = "";
	import { Router, Route } from "svelte-routing";
	import "smelte/src/tailwind.css" ;
	import Header from "./components/Header.svelte";
	import Footer from "./components/Footer.svelte";
	import Home from "./components/links/Home.svelte";
	import About from "./components/links/About.svelte";
	import Create from "./components/links/Create.svelte";
	import Memo from "./components/Memo.svelte";
</script>

<main class="bg-background-500">
	<Header/>
	<Router url="{url}">
		<div>
			<Route path="memo/:id" component="{Memo}"/>
			<Route path="create" component="{Create}"/>
			<Route path="about" component="{About}"/>
			<Route path="/"><Home/></Route>
		</div>
	</Router>
	<Footer/>
</main>

<style>

</style>