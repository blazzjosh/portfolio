<script>
	import githubLogo from './svgs/github.svg'
	import linkedinLogo from './svgs/linkedin.svg'
	import discordLogo from './svgs/discord.svg'
	import twitterLogo from './svgs/twitter.svg'
	let arr = [
		{ id: 1, href: "https://github.com/blazzjosh", src: githubLogo, name: "Github" },
		{ id: 2, href: "https://www.linkedin.com/in/horsfall-josh/", src: linkedinLogo, name: "Linkedin" }, 
		{ id: 3, href: "", src: discordLogo, name: "Discord" },
		{ id: 4, href: "https://twitter.com/Mr_Horsfall", src: twitterLogo, name: "Twitter" },


		];
</script>

<div
	class="max-w-sm mx-auto w-full flex justify-center items-center gap-2 flex-wrap dark:text-slate-400"
>
	{#each arr as { src, name, href}}
		<a {href} target="_blank" class="dark:text-slate-400 border p-2 flex items-center justify-center space-x-1">
			<!-- <object class="dark:bg-slate-400" data={src} title="" ></object> -->
			<img {src} class="dark:hidden" alt="">
			<div class="dark:text-teal-100">{name}</div>
		</a>
	{/each}
</div>
