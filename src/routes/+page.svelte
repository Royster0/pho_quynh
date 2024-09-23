<script>
	import { Hamburger } from "svelte-hamburgers";
	import Nav from "./components/Nav.svelte";
	import Header from "./components/Header.svelte";
	import About from "./components/About.svelte";
	import Menu from "./components/Menu.svelte";
	import Contact from "./components/Contact.svelte";
	import "../app.css";

	let open;
</script>

<div class="hamburger">
	<Hamburger
		bind:open
		--color="white"
	/>
</div>

<Nav bind:open />
<Header />
<About />
<Menu />
<Contact />

<style>
	.hamburger {
		position: fixed;
		top: 10px;
		left: 10px;
		z-index: 1001;
	}
</style>