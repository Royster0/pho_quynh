<script>
	import MenuItem from "../modules/MenuItem.svelte";

	const menuItems = {
		Appetizers: [
			{
				name: "Pot Stickers",
				desc: "Fried crescent dumpling",
				image: "/menu_items/pot_stickers.JPEG",
			},
		],
		Pho: [{}],
		Rice: [{}],
		Vermicelli: [{}],
	};
</script>

<section class="menu" id="menu">
	<div>
		<h2>Our Menu</h2>
		{#each Object.entries(menuItems) as [category, items]}
			<div class="category" id={category.toLowerCase().replace(/\s+/g, "-")}>
				<h3>{category}</h3>
				{#each items as item}
					<MenuItem image={item.image} name={item.name} desc={item.desc} />
				{/each}
			</div>
		{/each}
	</div>
</section>
