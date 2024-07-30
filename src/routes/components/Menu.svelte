<script>
	import MenuItem from "../modules/MenuItem.svelte";

	const menuItems = {
		Appetizers: [
			{
				name: "Gỏi Cuốn Tôm Thịt",
				desc: "Fresh Spring Rolls with Shrimp and Pork",
				image: "/menu_items/spring_rolls.avif",
				price: 8.49,
			},
			{
				name: "Gỏi Cuốn Nem Nướng",
				desc: "Fresh Spring Rolls with Pork Patties",
				image: "/menu_items/blank.png",
				price: 8.49,
			},
			{
				name: "Chả Giò",
				desc: "Egg Rolls",
				image: "/menu_items/egg_roll.avif",
				price: 9.0,
			},
			{
				name: "Gỏi Cuốn Đậu Hũ",
				desc: "Fresh Spring Rolls with Tofu",
				image: "/menu_items/blank.png",
				price: 8.99,
			},
			{
				name: "Cánh Gà",
				desc: "Sweet & Sour Chicken Wings",
				image: "/menu_items/blank.png",
				price: 10.05,
			},
			{
				name: "Cánh Gà Chiên Nước Mắm",
				desc: "Fish Sauce Chicken Wings",
				image: "/menu_items/blank.png",
				price: 9.55,
			},
			{
				name: "Bánh Bôt Loc",
				desc: "Fried Pot Stickers",
				image: "/menu_items/pot_stickers.avif",
				price: 8.99,
			},
			{
				name: "Mực Chiên",
				desc: "Fried Calamari",
				image: "/menu_items/fried_calamari.avif",
				price: 8.99,
			},
		],
		Vietnamese_Sandwiches: [
			{
				name: "Thịt Nướng",
				desc: "Grilled Pork",
			},
			{
				name: "Gà",
				desc: "Grilled Chicken",
			},
			{
				name: "Bò",
				desc: "Stir-Fried Beef",
			},
			{
				name: "Nem Nướng",
				desc: "Grilled Pork Patties",
			},
			{
				name: "Đậu Hủ",
				desc: "Fried Tofu",
			},
			{
				name: "Pho Burrito",
				desc: "Shredded beef, fresh greens, and vermicelli noodles wrapped in a spinach tortilla.",
			},
		],
		Pho: [
			{
				name: "Đặc Biệt",
				desc: "Round-eye Steak, Flank, Brisket, Tendon, Tripe and Meatball",
				image: "/menu_items/blank.png",
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
			{
				name: "Xương To",
				desc: "Tomahawk Pho",
				image: "/menu_items/tomahawk_pho.jpeg",
				price: 11.99,
			},
		],
		Rice_Dishes: [
			{
				name: "Com Đậu Hũ",
				desc: "Tofu Rice Dish",
				image: "/menu_items/com_dau_hu.jpeg",
				price: 11.99,
			},
			{
				name: "Com Sườn Nướng",
				desc: "Porkchop Rice Dish",
				image: "/menu_items/com_suon_heo.jpeg",
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
			{
				name: "Bánh Hỏi",
				desc: "Thin Vermicelli with Grilled Shrimp Wrapped Around Sugar Cane and Grilled Pork Patties",
				image: "/menu_items/banh_hoi.avif",
				price: 11.99,
			},
		],
		Dessert: [{}],
		Bubble_Tea: [{}],
	};
</script>

<section class="menu" id="menu">
	<div>
		<h2>Our Menu</h2>
		{#each Object.entries(menuItems) as [category, items]}
			<div class="category" id={category.toLowerCase().replace(/\s+/g, "-")}>
				<h3>{category.replace("_", " ")}</h3>
				{#if category == "Vietnamese_Sandwiches"}
					<div class="banh-mi-container">
						<p class="price">$9.00</p>
						<img
							src="/menu_items/banh_mi_thit_nuong.avif"
							alt="Banh Mi"
						/>
					</div>
				{/if}
				<div class="menu-item">
					{#each items as item}
						<MenuItem
							image={item.image}
							name={item.name}
							desc={item.desc}
							price={item.price}
						/>
					{/each}
				</div>
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

	.menu-item {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
	}

	.category {
		margin-bottom: 40px;
	}

	.category h3 {
		font-size: 2rem;
		margin-bottom: 20px;
		color: #f3f3f3;
	}

	.price {
		font-size: 1.4rem;
		font-weight: 700;
		color: #d0b457;
	}

	.banh-mi-container img {
		width: 100%;
		max-width: 50%;
		height: auto;
		border-radius: 7px;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
		transition: transform 0.3s;
	}

	.banh-mi-container img:hover {
		transform: scale(1.05);
	}
</style>
