<script>
	import "../app.css";
	import Nav from "../lib/components/Nav.svelte";
	let dark = true
</script>

<!-- This example requires Tailwind CSS v2.0+ -->
<div class:dark>
	<!-- We've used 3xl here, but feel free to try other max-widths based on your needs -->
<div class="w-full dark:bg-slate-900">
	<div class="max-w-3xl mx-auto border bg-white dark:bg-slate-900">
		<Nav bind:dark/>
		<slot />
	</div>
</div>

</div>
