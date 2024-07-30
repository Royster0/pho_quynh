<script>
	export let name;
	export let desc;
	export let image;
</script>

<div class="menu-item">
	<img src={image} alt={name} />
	<h4>{name}</h4>
	<p class="desc">{desc}</p>
</div>
