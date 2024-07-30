<script>
	import MenuItem from "../modules/MenuItem.svelte";

	const menuItems = {
		Appetizers: [
			{
				name: "Pot Stickers",
				desc: "Fried crescent dumpling",
				image: "/menu_items/pot_stickers.JPEG",
				price: 8.99,
			},
		],
		Pho: [
			{
				name: "Xương To",
				desc: "Tomahawk Pho",
				image: "/menu_items/tomahawk_pho.JPEG",
				price: 11.99,
			},
			{
				name: "Tái",
				desc: "Round-eye Steak Pho",
				image: "/menu_items/pho_tai.jpg",
				price: 11.99,
			},
			{
				name: "Chín, Bò Viên",
				desc: "Brisket, Meatball Pho",
				image: "/menu_items/pho_chin_bo_vien.jpg",
				price: 11.99,
			},
		],
		Rice: [
			{
				name: "Com Đậu Hũ",
				desc: "Tofu Rice Dish",
				image: "/menu_items/com_dau_hu.JPEG",
				price: 11.99,
			},
			{
				name: "Com Sườn Nướng",
				desc: "Porkchop Rice Dish",
				image: "/menu_items/com_suon_heo.JPEG",
				price: 11.99,
			},
		],
		Vermicelli: [
			{
				name: "Bún Thịt Nướng",
				desc: "Sliced Pork Vermicelli Bowl",
				image: "/menu_items/bun_thit_nuong.jpg",
				price: 11.99,
			},
		],
	};
</script>

<section class="menu" id="menu">
	<div>
		<h2>Our Menu</h2>
		{#each Object.entries(menuItems) as [category, items]}
			<div class="category" id={category.toLowerCase().replace(/\s+/g, "-")}>
				<h3>{category}</h3>
				{#each items as item}
					<MenuItem
						image={item.image}
						name={item.name}
						desc={item.desc}
						price={item.price}
					/>
				{/each}
			</div>
		{/each}
	</div>
</section>

<style>
	.menu {
		padding: 80px 20px;
		text-align: center;
		background-color: #003b46;
	}

	.menu h2 {
		font-size: 2.5rem;
		margin-bottom: 40px;
		color: #d0b457;
	}

	.category {
		margin-bottom: 40px;
	}

	.category h3 {
		font-size: 2rem;
		margin-bottom: 20px;
		color: #f3f3f3;
	}
</style>
