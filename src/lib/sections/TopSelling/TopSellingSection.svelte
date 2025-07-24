<script>
	import DestinationCard from './DestinationCard.svelte';

	const topDestinations = [
		{
			alt: 'Rome',
			country: 'Italy',
			price: '$5.42k',
			duration: '10 Days Trip',
			src: '/assets/imgs/Rectangle 14.png'
		},
		{
			alt: 'London',
			country: 'UK',
			price: '$4.2k',
			duration: '12 Days Trip',
			src: '/assets/imgs/Rectangle 15.png'
		},
		{
			alt: 'Full Europe',
			country: '',
			price: '$15k',
			duration: '28 Days Trip',
			src: '/assets/imgs/Rectangle 16.png'
		}
	];
</script>

<section class="top-selling py-16 text-center">
	<p class="section-subtitle mb-2 text-sm font-semibold text-[#5E6282] uppercase">Top Selling</p>
	<h2 class="section-title mb-16 font-serif text-[2.5rem] font-bold text-[#14183E]">
		Top Destinations
	</h2>

	<div class="grid grid-cols-[repeat(auto-fit,minmax(250px,1fr))] justify-items-center gap-8 px-8">
		{#each topDestinations as destination}
			<DestinationCard {...destination} />
		{/each}
	</div>
</section>
