<script lang="ts">
	import '../app.pcss';
	import { Button } from '$lib/components/ui/button';
	import * as Sheet from '$lib/components/ui/sheet';
	import hamburger from '$lib/assets/hamburgare.png';

	import { mediaQuery } from 'svelte-legos';

	const isDesktop = mediaQuery('(min-width: 768px)');
</script>

<div class="h-full w-screen">
	<slot />
</div>
