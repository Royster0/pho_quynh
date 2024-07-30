<script>
	let isMenuOpen = false;

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}
</script>

<nav>
	<div class="nav-item"><a href="#header">Home</a></div>
	<div class="nav-item"><a href="#about">About</a></div>
	<div class="nav-item">
		<a on:click={toggleMenu}>Menu</a>

		<div class="submenu" style:display={isMenuOpen ? "block" : "none"}>
			<a href="#appetizers">Appetizers</a>
			<a href="#pho">Pho</a>
			<a href="#rice">Rice Dishes</a>
			<a href="#vermicelli">Vermicelli</a>
		</div>
	</div>
	<div class="nav-item"><a href="#contact">Contact</a></div>
</nav>
<div class="spacer"></div>

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
		background-color: #003b46;
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

	.spacer {
		height: 70px;
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
