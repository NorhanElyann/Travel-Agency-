<script>
	const services = [
		{
			alt: 'Calculated Weather',
			description: 'Built Wicket longer admire do barton vanity itself do in it.',
			src: '/assets/imgs/satellite-dish.png',
			shapeClass: 'satellite'
		},
		{
			alt: 'Best Flights',
			description: 'Engrossed listening. Park gate sell they west hard for the.',
			src: '/assets/imgs/plane.png',
			shapeClass: 'plane'
		},
		{
			alt: 'Local Events',
			description: 'Barton vanity itself do in it. Preferred to men it engrossed listening.',
			src: '/assets/imgs/mic.png',
			shapeClass: 'mic'
		},
		{
			alt: 'Customization',
			description: 'We deliver outsourced aviation services for military customers.',
			src: '/assets/imgs/power-supply 1.png',
			shapeClass: 'power'
		}
	];
</script>

<section class="py-16 text-center ">
	<div class="mb-2 text-sm font-bold tracking-wide text-[#5E6282] uppercase">Category</div>
	<h2 class="font-volkhov mb-10 text-3xl font-bold text-[#14183E] md:text-4xl">
		We Offer Best Services
	</h2>

	<div class="grid grid-cols-1 gap-6 sm:grid-cols-2 lg:grid-cols-4">
		{#each services as { alt, description, src, shapeClass }}
			<div
				class="group relative overflow-hidden rounded-[15px] bg-white p-6 text-center transition-shadow hover:shadow-xl"
			>

				<!-- Icon -->
				<div class="relative z-10 mx-auto mb-4 flex h-20 w-20 items-center justify-center bg-white">
					<img
						{src}
						{alt}
						class={`max-h-[60px] max-w-[60px] object-contain ${shapeClass === 'plane' ? 'max-h-[100px] max-w-[100px]' : ''}`}
					/>
				</div>

				<!-- Title -->
				<h3 class="mb-2 text-base font-semibold text-[#181E4B]">{alt}</h3>
				<p class="relative z-10 text-sm leading-relaxed text-[#5E6282]">{description}</p>
			</div>
		{/each}
	</div>
</section>


