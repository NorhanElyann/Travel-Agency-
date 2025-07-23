<script>
	// data testimonials
	const testimonials = $state([
		{
			src: '/assets/imgs/Mike.png',
			alt: 'Mike Taylor',
			text: 'On the Windows talking painted pasture yet its express parties use. Sure last upon he same as knew next. Of believed or diverted no.',
			author: 'Mike Taylor',
			location: 'Lahore, Pakistan'
		},
		{
			src: '/assets/imgs/Chris.png',
			alt: 'Chris Thomas',
			text: 'Great service and amazing experience! Highly recommend for travel planning.',
			author: 'Chris Thomas',
			location: 'CEO of Red Button'
		},
		{
			src: '/assets/imgs/Sarah.png',
			alt: 'Sarah Johnson',
			text: 'Affordable trips with excellent support. Will book again!',
			author: 'Sarah Johnson',
			location: 'New York, USA'
		}
	]);

	// control slider
	let currentTestimonial = $state(0);
	const totalTestimonials =$derived(testimonials.length) ;

	let nextIndex = $derived((currentTestimonial + 1) % totalTestimonials);
	let prevIndex = $derived((currentTestimonial - 1 + totalTestimonials) % totalTestimonials);

	const showTestimonial = (index)  => currentTestimonial = index;
	const nextTestimonial = () => currentTestimonial = nextIndex;
	const prevTestimonial = () => currentTestimonial = prevIndex;
	
</script>

<section class="mx-auto px-8 py-16 ">
	<div class="flex flex-wrap justify-center gap-10">
		<!-- LEFT SIDE: Title -->
		<div class="min-w-[40%] flex-1">
			<h3 class="mb-4 text-lg font-semibold text-gray-600">TESTIMONIALS</h3>
			<h2 class="mb-6 font-['Volkhov',serif] text-4xl leading-tight font-bold text-[#14183E]">
				What People Say <br /> About Us.
			</h2>
		</div>

		<!-- RIGHT SIDE: Testimonial Cards -->
		<div class="relative min-w-[55%] flex-1">
			<div class="relative top-[100px] h-[400px] w-[550px] md:top-0">
				{#each testimonials as {src,alt,text,author,location}, index}
					<div
						class="absolute h-[200px] w-full rounded-[10px] bg-white p-8 shadow-[0_4px_12px_rgba(0,0,0,0.1)] transition-all  duration-400 ease-in-out
                            {index === currentTestimonial
							? 'top-0 z-[2]'
							: index === nextIndex
								? 'top-[90px] left-10 z-[1] bg-[#F6F6F6]'
								: 'opacity-0'}"
					>
						<img
							{src}
							{alt}
							class="absolute top-[-30px] left-[-30px] h-[70px] w-[70px] rounded-full shadow-[0_0_0_2px_#e2e8f0] "
						/>
						<p class="mt-4 mb-4 max-h-[120px] text-base leading-6 text-[#475569]">
							"{text}"
						</p>
						<p class="mb-1 font-semibold text-[#1e293b]">{author}</p>
						<p class="text-sm text-[#64748b]">{location}</p>
					</div>
				{/each}

				<!-- Navigation Buttons -->
				<div
					class="absolute top-[20%] right-[-80px] flex flex-col gap-4 md:top-[150px] md:right-auto md:left-[610px]"
				>
					<button
						class="cursor-pointer border-none bg-transparent text-lg text-[#BCB7C2]"
						onclick={prevTestimonial}
					>
						<i class="fas fa-chevron-up"></i>
					</button>
					<button
						class="cursor-pointer border-none bg-transparent text-lg text-[#3E2E4D]"
						onclick={nextTestimonial}
					>
						<i class="fas fa-chevron-down"></i>
					</button>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	@media (max-width: 750px) {
		.flex {
			flex-direction: column;
			align-items: center;
		}

		.min-w-\[40\%\],
		.min-w-\[55\%\] {
			width: 100%;
			text-align: center;
		}

		.w-\[550px\] {
			width: 90%;
			height: 350px;
			top: 0;
		}

		.h-\[200px\] {
			height: 250px;
			padding: 1rem;
		}
	}
</style>
