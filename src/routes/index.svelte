<script>
	import He from "../lib/components/Header.svelte";
	import GridCards from "../lib/components/QuickLinks.svelte";
	import Government from "../lib/components/Government.svelte";
	import Projects from "../lib/components/Projects.svelte";
	import SkillsGrid from "../lib/components/SkillsGrid.svelte"
	let links = [
		{ name: "resume", href: "" },
		{ name: "github", href: "" },
	];

	let projects = [];

	let skills = [];
</script>

<section class="w-full flex-col justify-center items-center">
	<div
		class="mx-auto flex-col space-y-28 text-center py-16 px-4 sm:py-20 sm:px-6 lg:px-8"
	>
		<section>
			<h2 class="text-4xl font-extrabold text-gray-500 sm:text-4xl">
				<span class="block">Hi friend,</span>
			</h2>

			<p>
				I'm Josh from 🇳🇬Nigeria and I'm infinitely curious at how things
				work but mostly passionate about ☕ JavaScript and 🎨 UI/UX.
			</p>
		</section>

		<section>
			<He name="Quick Links" />
			<div class="m-2 flex justify-center">
				<GridCards />
			</div>
		</section>

		<section>
			<He name="Skills" />
			
			<SkillsGrid/>
		</section>

		<section id="projects">
			<He name="Projects" />
			<Projects/>
		</section>

		<section id="govt" class="text-left">
			<Government />
		</section>
	</div>
</section>
