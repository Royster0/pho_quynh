<script>
	import { fade, fly } from "svelte/transition";

	export let open;
	let isSubMenuOpen = false;

	function toggleSubMenu() {
		isSubMenuOpen = !isSubMenuOpen;
	}
</script>

{#if open}
<nav class="nav" in:fade={{ duration: 130 }} out:fade={{ duration: 150 }}>
	<div class="nav-item" transition:fly={{ y: '100%', delay: 50 }} >
		<a href="#header">Home</a>
	</div>
	<div class="nav-item" transition:fly={{ y: '100%', delay: 100 }} >
		<a href="#about">About</a>
	</div>
	<div class="nav-item" transition:fly={{ y: '100%', delay: 150 }} >
		<!-- svelte-ignore a11y-click-events-have-key-events -->
		<!-- svelte-ignore a11y-no-static-element-interactions -->
		<!-- svelte-ignore a11y-missing-attribute -->
		<a on:click={toggleSubMenu}>Menu</a>

		<div class="submenu" style:display={isSubMenuOpen ? "block" : "none"}>
			<a href="#appetizers">Appetizers</a>
			<a href="#vietnamese_sandwiches">Banh Mi</a>
			<a href="#pho">Pho</a>
			<a href="#rice_dishes">Rice Dishes</a>
			<a href="#vermicelli">Vermicelli</a>
			<a href="#dessert">Dessert</a>
			<a href="#bubble_tea">Bubble Tea</a>
		</div>
	</div>
	<div class="nav-item" transition:fly={{ y: '100%', delay: 200 }} >
		<a href="#contact">Contact</a>
	</div>
</nav>
{/if}

<style>
	nav {
		display: flex;
		justify-content: space-around;
		align-items: center;
		background-color: rgba(0, 0, 0, 0.9);
		padding: 10px 20px;
		position: fixed;
		width: 100%;
		top: 0;
		z-index: 1000;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
	}

	nav a {
		color: white;
		padding: 14px 50px;
		font-size: 1.2rem;
		transition: background-color 0.3s;
		position: relative;
	}

	nav a:hover {
		background-color: #d0b457;
	}

	.nav-item {
		position: relative;
		margin: 15px 15px;
	}

	.submenu {
		display: none;
		position: absolute;
		top: 170%;
		left: 0;
		background-color: #1f4653;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
		overflow: hidden;
	}

	.submenu a {
		display: block;
		padding: 10px 20px;
		color: white;
	}

	.submenu a:hover {
		background-color: #d0b457;
	}

	.nav-item:hover .submenu {
		display: block;
	}

	@media (max-width: 768px) {
		nav {
			flex-direction: column;
		}

		.nav-item {
			width: 100%;
			text-align: center;
		}

		.submenu {
			position: static;
			width: 100%;
			margin-top: 15px;
		}
	}
</style>
