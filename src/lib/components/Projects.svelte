<script>
	import logo from './svgs/github.svg'


	let projects = [
		{id:1, name: 'CloudDocs', category: 'Office', href: 'https://github.com/', src: 'https://github.com/', desc: 'A permission based cloud storage web solution for office use'},
		{id:2, name: 'SupplyBox', category: 'Internal', href: 'https://github.com/', src: 'https://github.com/', desc: 'A web application for supplier management'},
		{id:3, name: 'TaskFlow', category: 'Productivity', href: 'https://github.com/', src: 'https://github.com/', desc: 'A web application for robust task management and rating'},
		{id:4, name: 'CaterGo', category: 'Inventory', href: 'https://github.com/', src: 'https://github.com/', desc: 'A catering web application with inventory used in offshore locations'}


	]
</script>

<ul class='flex justify-center flex-wrap gap-8'>
	{#each projects as {name, category, href, src, desc}}
		<li class="text-left py-2 ">
			<div class="flex w-64 flex-col justify-center bg-white dark:bg-slate-800 rounded-2xl shadow-xl shadow-slate-300/60">
				<img
					class="border dark:border-0 p-2 aspect-[3/1] w-full rounded-t-2xl object-contain"
					src={logo}
					alt="screenshot"
				/>

				<div class="p-4">
					<small class="text-teal-400 text-xs"
						>{category}</small
					>
					<h1 class="text-2xl font-medium text-slate-600 pb-2 dark:text-teal-100">
						{name}
					</h1>
					<p
						class="text-sm tracking-tight font-light text-slate-400 leading-6"
					>
					{desc}
					</p>
					<div class="flex justify-end text-slate-400">
						<a {href} target="_blank">
							<svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 hover:text-slate-600" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
								<path stroke-linecap="round" stroke-linejoin="round" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
							  </svg>
						</a>
					</div>
				</div>
			</div>
		</li>
	{/each}
</ul>

