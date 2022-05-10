<script>
	let showMenu = false;
</script>

<header class="bg-white shadow">
	<div class="mx-auto px-2 sm:px-4 lg:divide-y lg:divide-gray-200 lg:px-8 ">
		<div class="relative h-16 flex justify-between">
			<!-- logo -->
			<div class="relative z-10 px-2 flex lg:px-0 ">
				<div class="flex-shrink-0 flex items-center">
					<span
						class="text-teal-400 font-extrabold flex items-center px-2 py-2 leading-5"
						>@Jorsh</span
					>
				</div>
			</div>
			<!-- logo -->

			<div class="relative z-10 flex items-center lg:hidden">
				{#if showMenu}
					<button
						on:click={() => (showMenu = !showMenu)}
						class="rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-teal-500"
					>
						<svg
							class="block h-6 w-6"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="2"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M6 18L18 6M6 6l12 12"
							/>
						</svg>
					</button>
				{:else}
					<button
						on:click={() => (showMenu = !showMenu)}
						type="button"
						class="rounded-md p-2 inline-flex items-center justify-center text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-teal-500"
						aria-controls="mobile-menu"
						aria-expanded="false"
					>
						<span class="sr-only">Open menu</span>
						<svg
							class="block h-6 w-6"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="2"
							stroke="currentColor"
							aria-hidden="true"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M4 6h16M4 12h16M4 18h16"
							/>
						</svg>
					</button>
				{/if}
			</div>

			<div
				class="hidden space-x-2 lg:relative lg:z-10 lg:ml-4 lg:flex lg:items-center"
			>
				<button
					type="button"
					class="flex-shrink-0 bg-white rounded-full p-1 text-gray-400 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-teal-500"
				>
					<span class="sr-only">View notifications</span>

					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="h-6 w-6"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						stroke-width="2"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M20.354 15.354A9 9 0 018.646 3.646 9.003 9.003 0 0012 21a9.003 9.003 0 008.354-5.646z"
						/>
					</svg>
				</button>

				<button
					type="button"
					class="flex-shrink-0 bg-white rounded-full p-1 text-gray-400 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-teal-500"
				>
					<span class="sr-only">View notifications</span>

					<svg
						class="h-6 w-6"
						xmlns="http://www.w3.org/2000/svg"
						fill="none"
						viewBox="0 0 24 24"
						stroke-width="2"
						stroke="currentColor"
						aria-hidden="true"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"
						/>
					</svg>
				</button>

				<button
					type="button"
					class="flex-shrink-0 bg-white rounded-full p-1 text-gray-400 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-teal-500"
				>
					<span class="sr-only">View notifications</span>

					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="h-6 w-6"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						stroke-width="2"
					>
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
						/>
					</svg>
				</button>
			</div>
		</div>
		<nav class="hidden lg:py-2 lg:flex lg:space-x-8" aria-label="Global">
			<!-- Current: "bg-gray-100 text-gray-900", Default: "text-gray-900 hover:bg-gray-50 hover:text-gray-900" -->
			
			<a
				href="##"
				class="text-gray-900 hover:bg-gray-50 hover:text-gray-900 rounded-md py-2 px-3 inline-flex items-center text-sm font-medium"
			>
				Projects
			</a>


			<a
				href="#govt"
				class="text-gray-900 hover:bg-gray-50 hover:text-gray-900 rounded-md py-2 px-3 inline-flex items-center text-sm font-medium"
			>
				REPL
			</a>
		</nav>
	</div>

	<!-- Mobile menu, show/hide based on menu state. -->
	{#if showMenu}
		<nav class="lg:hidden" aria-label="Global" id="mobile-menu">
			<div class="pt-2 pb-3 px-2 space-y-1">
				<!-- Current: "bg-gray-100 text-gray-900", Default: "text-gray-900 hover:bg-gray-50 hover:text-gray-900" -->
				<a
					href="##"
					class="bg-gray-100 text-gray-900 block rounded-md py-2 px-3 text-base font-medium"
					aria-current="page">Dashboard</a
				>

				<a
					href="##"
					class="text-gray-900 hover:bg-gray-50 hover:text-gray-900 block rounded-md py-2 px-3 text-base font-medium"
					>Team</a
				>

				<a
					href="##"
					class="text-gray-900 hover:bg-gray-50 hover:text-gray-900 block rounded-md py-2 px-3 text-base font-medium"
					>Projects</a
				>

				<a
					href="##"
					class="text-gray-900 hover:bg-gray-50 hover:text-gray-900 block rounded-md py-2 px-3 text-base font-medium"
					>Calendar</a
				>
			</div>
		</nav>
	{/if}
</header>
