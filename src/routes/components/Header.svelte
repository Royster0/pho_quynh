<section class="header" id="header">
	<div class="overlay"></div>
	<div class="content">
		<h1>Welcome to Phở Quỳnh</h1>
	</div>
</section>

<style>
	.header {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 90vh;
		background-image: url("/menu_items/pho_img.png");
		background-size: cover;
		background-position: center;
		color: #d0b457;
		text-align: center;
		position: relative;
	}

	.overlay {
		position: absolute;
		top: 0;
		bottom: 0;
		left: 0;
		right: 0;
		background: rgba(0, 0, 0, 0.5);
	}

	.content {
		position: relative;
		z-index: 1;
	}

	.header h1 {
		font-size: 4rem;
		margin-bottom: 20px;
		animation: fadeInDown 1s ease-in-out;
	}

	@keyframes fadeInDown {
		from {
			opacity: 0;
			transform: translateY(-20px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}
</style>
