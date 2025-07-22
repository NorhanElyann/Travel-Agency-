<script lang="ts">

    interface FooterLink {
		title: string;
		links: string[];
	}

	const footerLinks: FooterLink[] = [
		{
			title: 'Company',
			links: ['About', 'Careers', 'Mobile']
		},
		{
			title: 'Contact',
			links: ['Help/FAQ', 'Press', 'Affiliates']
		},
		{
			title: 'More',
			links: ['Airlinefees', 'Airline', 'Low fare tips']
		}
	];
</script>

<footer class="px-4 py-12 text-center">
	<div
		class="mx-auto flex max-w-7xl flex-wrap items-start justify-around gap-6 sm:flex-col md:flex-row md:justify-between sm:items-center sm:gap-6  md:gap-8"
	>
		<!-- Logo and Description -->
		<div
			class="flex flex-col text-left sm:mb-12 sm:max-w-[350px] sm:text-center md:max-w-[350px] md:text-center"
		>
			<h4 class="mb-4 text-5xl font-medium text-black">Jadoo.</h4>
			<p class="text-sm leading-6 text-[#5E6282]">
				Book your trip in minutes, get full<br /> control for much longer.
			</p>
		</div>

		<!-- Footer Links -->
		<div
			class="flex gap-6 text-left sm:mb-12 sm:max-w-[350px] sm:justify-center sm:text-center md:max-w-[350px] md:gap-8 md:text-center"
		>
			{#each footerLinks as linkGroup}
				<div>
					<h4 class="mb-6 text-base text-black sm:text-lg md:text-lg">
						{linkGroup.title}
					</h4>
					<ul class="list-none p-0">
						{#each linkGroup.links as link}
							<li
								class="mb-2 cursor-pointer text-sm text-[#5E6282] hover:text-[#fa7436] sm:text-base md:text-base"
							>
								{link}
							</li>
						{/each}
					</ul>
				</div>
			{/each}
		</div>

		<!-- Social and App -->
		<div class="text-left sm:mb-12 sm:max-w-[350px] sm:text-center md:max-w-[350px] md:text-center">
			<div class="mb-4 flex gap-2.5 sm:justify-center md:justify-center">
				<a
					href="#"
					class="flex h-[35px] w-[35px] items-center justify-center rounded-full bg-white text-[#181E4B] no-underline shadow-[0_2px_6px_rgba(0,0,0,0.1)] transition-all duration-300 hover:bg-gradient-to-r hover:from-[#fa7436] hover:to-[#fc964a] hover:text-white"
				>
					<i class="fab fa-facebook-f"></i>
				</a>
				<a
					href="#"
					class="flex h-[35px] w-[35px] items-center justify-center rounded-full bg-white text-[#181E4B] no-underline shadow-[0_2px_6px_rgba(0,0,0,0.1)] transition-all duration-300 hover:bg-gradient-to-r hover:from-[#fa7436] hover:to-[#fc964a] hover:text-white"
				>
					<i class="fab fa-instagram"></i>
				</a>
				<a
					href="#"
					class="flex h-[35px] w-[35px] items-center justify-center rounded-full bg-white text-[#181E4B] no-underline shadow-[0_2px_6px_rgba(0,0,0,0.1)] transition-all duration-300 hover:bg-gradient-to-r hover:from-[#fa7436] hover:to-[#fc964a] hover:text-white"
				>
					<i class="fab fa-twitter"></i>
				</a>
			</div>
			<p class="mb-2 text-[0.95rem] font-semibold text-[#3f3d56] sm:mb-4">Discover our app</p>
			<div class="mt-4 flex gap-4 sm:flex-col sm:gap-2 md:flex-row md:justify-center md:gap-4">
				<a
					href="#"
					class="flex h-[35px] items-center rounded-[20px] bg-black px-3 py-2 text-white no-underline transition-transform duration-300 hover:scale-105 sm:justify-center md:justify-center"
				>
					<i class="fab fa-google-play mr-2 text-[1.3rem]"></i>
					<div class="flex flex-col leading-none">
						<span class="text-[0.5rem] opacity-80 sm:text-[0.65rem] md:text-[0.65rem]"
							>Get it on</span
						>
						<strong class="text-[0.5rem] sm:text-[0.65rem] md:text-[0.65rem]">Google Play</strong>
					</div>
				</a>
				<a
					href="#"
					class="flex h-[35px] items-center rounded-[20px] bg-black px-3 py-2 text-white no-underline transition-transform duration-300 hover:scale-105 sm:justify-center md:justify-center"
				>
					<i class="fab fa-apple mr-2 text-[1.3rem]"></i>
					<div class="flex flex-col leading-none">
						<span class="text-[0.5rem] opacity-80 sm:text-[0.65rem] md:text-[0.65rem]"
							>Available on</span
						>
						<strong class="text-[0.5rem] sm:text-[0.65rem] md:text-[0.65rem]">App Store</strong>
					</div>
				</a>
			</div>
		</div>
	</div>

	<p class="mt-12 mb-10 text-base text-[#5E6282] sm:mt-8">All rights reserved@jadoo.co</p>
</footer>
