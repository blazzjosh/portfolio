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

<svelte:head>
	<title>Cradly Josh</title>
</svelte:head>
<section class="w-full flex-col justify-center items-center">
	<div
		class="mx-auto flex-col space-y-28 text-center py-16 px-4 sm:py-20 sm:px-6 lg:px-8"
	>
		<section>
	
			<h2 class="text-4xl font-extrabold text-gray-500 sm:text-4xl">
				<span class="block dark:text-teal-300">Hello! I'm Josh,</span>
			</h2>
					<p class="p-4 dark:text-slate-300">
						I enjoy working closely with product and design to create amazing, polished user experiences, 
						and will often go the extra mile to include whimsical touches; i'm mostly passionate about ☕  JavaScript and 🎨 UI/UX.
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
