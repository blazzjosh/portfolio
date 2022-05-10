<script>
	import "../app.css";
	import Nav from "../lib/components/Nav.svelte";
</script>

<!-- This example requires Tailwind CSS v2.0+ -->
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 bg-gray-800">
	<!-- We've used 3xl here, but feel free to try other max-widths based on your needs -->
	<div class="max-w-3xl mx-auto border bg-white">
		<Nav />
		<slot />
	</div>
</div>
