<script>
	import htmlLogo from "./svgs/html.svg";
	import cssLogo from "./svgs/css.svg"
	import jsLogo from "./svgs/js.svg"

	let arr2 = [
		{ id: 1, name: "html", src: htmlLogo },
		{ id: 2, name: "css", src: cssLogo },
		{ id: 3, name: "Js", src: jsLogo },
		{ id: 4, name: "tailwind", src: "" },
		{ id: 5, name: "git", src: "" },
		{ id: 6, name: "svelte", src: "" },
		{ id: 7, name: "sveltekit", src: "" },
		{ id: 1, name: "aws", src: "" },
	];

</script>

<div
	class="max-w-sm mx-auto w-full flex justify-center items-center gap-2 flex-wrap"
>
	{#each arr2 as { name, src }}
		<div class="border p-2">
			<!-- <img {src} alt="" /> -->
			<span class="dark:text-teal-100 uppercase text-gray-600">{name}</span>
		</div>
	{/each}
</div>
