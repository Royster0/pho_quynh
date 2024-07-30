<script>
	export let name;
	export let desc;
	export let image;
	export let price;
</script>

<div class="menu-item">
	<img src={image} alt={name} />
	<p class="name">{name}</p>
	<p class="desc">{desc}</p>
	<p class="price">${price}</p>
</div>

<style>
	.menu-item {
		display: inline-block;
		margin: 20px;
		max-width: 250px;
		text-align: center;
	}

	.menu-item img {
		width: 100%;
		height: auto;
		border-radius: 7px;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
		transition: transform 0.3s;
	}

	.menu-item img:hover {
		transform: scale(1.05);
	}

	.menu-item .name {
		margin-top: 10px;
		font-size: 1.3rem;
		font-weight: bold;
		color: #f3f3f3;
	}

	.menu-item .desc {
		font-size: 1.1rem;
		color: #d6d6d6;
		margin-top: 5px;
	}

	.menu-item .price {
		font-size: 1.2rem;
		font-weight: 500;
		color: #d0b457;
	}
</style>
