<script>
	export let imageSrc;
	export let altText;
	let enlarged = false;

	function toggleSize() {
		enlarged = !enlarged;
	}
</script>

<div>
	<button on:click={toggleSize}>
		<img
			src={imageSrc}
			alt={altText}
			class="object-cover {enlarged ? 'fixed top-12 z-20 h-screen w-screen' : 'sm:w-5/6'}"
		/>
	</button>
</div>
