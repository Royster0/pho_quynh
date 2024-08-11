<script>
	import MenuItem from "../modules/MenuItem.svelte";

	const menuItems = {
		Appetizers: [
			{
				name: "Gỏi Cuốn Tôm Thịt",
				desc: "Fresh Spring Rolls with Shrimp and Pork",
				image: "/menu_items/blank.png",
				price: "8.49",
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
				image: "/menu_items/blank.png",
				price: "9.00",
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
				name: "Bánh Khọt",
				desc: "Mini Savory Pancakes (Only available on weekdays!)",
				image: "/menu_items/banh-khot.png",
				price: 18.95,
			},
			{
				name: "Bánh Bôt Loc",
				desc: "Fried Pot Stickers",
				image: "/menu_items/potstickers.png",
				price: 9.45,
			},
			{
				name: "Mực Chiên",
				desc: "Fried Calamari",
				image: "/menu_items/blank.png",
				price: 8.99,
			},
			{
				name: "Đậu Hũ Chiên",
				desc: "Fried Tofu with Garlic",
				image: "/menu_items/blank.png",
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
				price: 14.99,
			},
			{
				name: "Tái",
				desc: "Round-eye Steak Pho",
				image: "/menu_items/blank.png",
				price: 14.99,
			},
			{
				name: "Chín, Bò Viên",
				desc: "Brisket, Meatball Pho",
				image: "/menu_items/blank.png",
				price: 14.99,
			},
			{
				name: "Xương To",
				desc: "Tomahawk Pho",
				image: "/menu_items/tomahawk-pho.png",
				price: 18.99,
			},
		],
		Rice_Dishes: [
			{
				name: "Cơm Đặc Biệt (Sườn, Bì, Chả, Trứng, Tôm)",
				desc: "Broken Rice Plate with Grilled Pork Chop, Shredded Pork, Meat Cake and Prawns",
				image: "/menu_items/blank.png",
				price: 16.35,
			},
			{
				name: "Com Sườn Heo",
				desc: "Grilled Porkchop Rice Dish",
				image: "/menu_items/com-suon-heo.png",
				price: 15.95,
			},
			{
				name: "Cơm Gà Nướng, Chả Giò",
				desc: "Grilled Chicken Rice Dish with Egg Roll",
				image: "/menu_items/blank.png",
				price: 15.55,
			},
			{
				name: "Cơm Sườn Bò Nướng",
				desc: "Grilled Marinated Beef Rice Dish",
				image: "/menu_items/blank.png",
				price: 15.45,
			},
			{
				name: "Cơm Tôm Nướng Chả Giò",
				desc: "Grilled Prawn Rice Dish with Egg Roll",
				image: "/menu_items/blank.png",
				price: 15.45,
			},
			{
				name: "Cơm Thịt Nướng Hoặc Nem Nướng",
				desc: "Grilled Porkchop and Pork Patty Rice Dish",
				image: "/menu_items/blank.png",
				price: 15.45,
			},
			{
				name: "Com Đậu Hũ",
				desc: "Tofu Rice Dish",
				image: "/menu_items/com-tofu.png",
				price: 11.99,
			},
			{
				name: "Cơm Sườn Bì, Đậu Hũ Ky",
				desc: "Grilled Porkchop, Shredded Pork, and Bean Curd Rice Dish",
				image: "/menu_items/blank.png",
				price: 15.95,
			},
			{
				name: "Gà Teriyaki",
				desc: "Chicken Teriyaki",
				image: "/menu_items/blank.png",
				price: 15.55,
			},
			{
				name: "Cơm Chiên",
				desc: "Fried Rice with Chicken, Shrimp, Eggs, and Broccoli",
				image: "/menu_items/blank.png",
				price: 18.45,
			},
			{
				name: "Cơm Bò Xào",
				desc: "Stir-Fried Beef with Bell Pepper, Onion, and Rice",
				image: "/menu_items/blank.png",
				price: 15.95,
			},
			{
				name: "Cơm Cá Hồi",
				desc: "Grilled Salmon and Veggies Rice Dish",
				image: "/menu_items/blank.png",
				price: 16.95,
			},
		],
		Vermicelli: [
			{
				name: "Bún Bì, Thịt Nướng",
				desc: "Shredded Pork Vermicelli Bowl",
				image: "/menu_items/blank.png",
				price: 14.65,
			},
			{
				name: "Bún Nem Nướng Chả Giò",
				desc: "Grilled Pork Patty Vermicelli Bowl with Egg Roll",
				image: "/menu_items/blank.png",
				price: 15.15,
			},
			{
				name: "Bún Thịt Nướng Chả Giò",
				desc: "Sliced Pork Vermicelli Bowl with Egg Roll",
				image: "/menu_items/blank.png",
				price: 15.05,
			},
			{
				name: "Bún Gà Nướng Chả Giò",
				desc: "Grilled Chicken Vermicelli Bowl with Egg Roll",
				image: "/menu_items/blank.png",
				price: 15.05,
			},
			{
				name: "Bún Tôm Nướng Chả Giò",
				desc: "Grilled Prawn Vermicelli Bowl with Egg Roll",
				image: "/menu_items/blank.png",
				price: 15.95,
			},
			{
				name: "Bún Tôm, Thịt Nướng",
				desc: "Grilled Prawn and Shredded Pork Vermicelli Bowl with Egg Roll",
				image: "/menu_items/blank.png",
				price: 15.45,
			},
			{
				name: "Bún Chả Giò",
				desc: "Egg Roll Vermicelli Bowl",
				image: "/menu_items/blank.png",
				price: 15.05,
			},
			{
				name: "Bún Đậu Hũ",
				desc: "Tofu Vermicelli Bowl",
				image: "/menu_items/blank.png",
				price: 15.05,
			},
			{
				name: "Bún Bò Xào",
				desc: "Stir-Fry Beef and Onion Vermicelli Bowl",
				image: "/menu_items/blank.png",
				price: 15.95,
			},
			{
				name: "Mì Xào",
				desc: "Stir-Fry Noodles",
				image: "/menu_items/blank.png",
				price: 15.95,
			},
			{
				name: "Bánh Hỏi",
				desc: "Thin Vermicelli with Grilled Shrimp Wrapped Around Sugar Cane and Grilled Pork Patties",
				image: "/menu_items/blank.png",
				price: 18.45,
			},
		],
		Dessert: [
			{
				name: "Chè Ba Mầu",
				desc: "Red Bean, Yellow Mung Bean, and Green Jelly topped with Coconut Cream",
				image: "/menu_items/blank.png",
				price: "5.50",
			},
			{
				name: "Chè Đậu Đà Lạt",
				desc: "White Bean, Green Jelly topped with Coconut Cream",
				image: "/menu_items/blank.png",
				price: "5.50",
			},
			{
				name: "Chè Đậu Đỏ",
				desc: "Red Bean, Green Jelly topped with Coconut Cream",
				image: "/menu_items/blank.png",
				price: "5.50",
			},
		],
		Bubble_Tea: [
			{
				name: "Avocado",
				desc: "Quả Bơ",
			},
			{
				name: "Durian",
				desc: "sầu riêng",
			},
			{
				name: "Papaya",
				desc: "Ðu Ðủ",
			},
			{
				name: "Mango",
				desc: "Xoài",
			},
			{
				name: "Strawberry",
				desc: "Dâu",
			},
			{
				name: "Taro",
				desc: "Khoai Môn",
			},
			{
				name: "Honeydew",
				desc: "Dưa Gang",
			},
			{
				name: "Watermelon",
				desc: "Dưa Hấu",
			},
			{
				name: "Soursop",
				desc: "Mãng Cầu",
			},
			{
				name: "Thai Tea",
				desc: "Trà Thái",
			},
		],
	};
</script>

<section class="menu" id="menu">
	<div>
		<h2>Our Menu</h2>
		{#each Object.entries(menuItems) as [category, items]}
			<div class="category" id={category.toLowerCase().replace(/\s+/g, "-")}>
				<h3>{category.replace("_", " ")}</h3>
				{#if category == "Vietnamese_Sandwiches"}
					<div class="single-image-container">
						<p class="price">$8.00</p>
						<img
							src="/menu_items/banh-mi-temp.png"
							alt="Banh Mi Thit Nuong"
						/>
					</div>
				{/if}
				{#if category == "Bubble_Tea"}
					<div class="single-image-container">
						<p class="price">$6.05</p>
						<p class="sub-text">
							With your choice of: <b>Tapioca</b>, <b>Crystal Boba</b>,
							<b>Coconut Jelly</b>, or
							<b>Rainbow Jelly</b>
						</p>
						<p class="sub-text">$0.85 per topping</p>
						<img src="/menu_items/bubble-tea-temp.png" alt="Bubble Tea" />
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
		background-color: #113f51;
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

	.single-image-container img {
		max-width: 40%;
		height: auto;
		border-radius: 7px;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
		transition: transform 0.3s;
	}

	.single-image-container img:hover {
		transform: scale(1.05);
	}

	.sub-text {
		color: #d6d6d6;
		font-size: 1.1rem;
	}
</style>
