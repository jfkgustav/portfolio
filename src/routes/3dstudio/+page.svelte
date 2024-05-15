<script>
	import ImageZoom from '$lib/components/ImageZoom.svelte';
	import skrivert_skriva from '$lib/assets/skrivert/skriva.png';
	let altTextSkrivert = 'skrivert skriva';
	let imgSrc = 'src/lib/assets/skrivert/skriva.png';
</script>

<ImageZoom bind:imageSrc={imgSrc} bind:altText={altTextSkrivert} />
