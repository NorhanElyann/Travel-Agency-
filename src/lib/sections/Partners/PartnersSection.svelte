<script>
	const partners = [
		{ src: '/assets/imgs/axon.png', alt: 'Axon Airlines' },
		{ src: '/assets/imgs/jetstar.png', alt: 'Jetstar' },
		{ src: '/assets/imgs/expedia_logo.png', alt: 'Expedia' },
		{ src: '/assets/imgs/Qantas-Logo.png', alt: 'Qantas' },
		{ src: '/assets/imgs/Alitalia-Logo.png', alt: 'Alitalia' }
	];
</script>

<section class="mx-auto px-8 py-16 sm:px-6 lg:px-8">
	<div class="flex flex-wrap justify-center gap-10">
		{#each partners as  {src,alt}}
			<div
				class="flex h-[180px] w-[180px] items-center justify-center overflow-hidden rounded-xl transition-transform duration-300 ease-in hover:scale-110 hover:bg-white hover:shadow-[0_15px_40px_rgba(0,0,0,0.07)] sm:h-[150px] sm:w-[150px] md:h-[200px] md:w-[200px]"
			>
				<img
					{src}
					{alt}
					class="max-h-full max-w-full object-contain opacity-90 grayscale transition-all duration-300 ease-in hover:opacity-100 hover:grayscale-0 sm:opacity-100 sm:grayscale-0"
				/>
			</div>
		{/each}
	</div>
</section>
