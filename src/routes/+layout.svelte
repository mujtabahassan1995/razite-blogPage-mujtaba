<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';
	import Navbar from "$lib/components/Navbar.svelte";

	let { children } = $props();

</script>


<header class="w-full">
	<Navbar />
</header>


<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>
	
{@render children?.()}
<footer>
	<p>&copy; 2024 My Website. All rights reserved.</p>
</footer>