<script lang="ts">
	interface Step {
		icon: string;
		title: string;
		description: string;
		bg: string;
	}

	const steps: Step[] = [
		{
			icon: 'fa-object-group',
			title: 'Choose Destination',
			description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Urna, tortor tempus.',
			bg: 'bg-[#F0BB1F]'
		},
		{
			icon: 'fa-person-swimming',
			title: 'Make Payment',
			description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Urna, tortor tempus.',
			bg: 'bg-[#F15A2B]'
		},
		{
			icon: 'fa-taxi',
			title: 'Reach Airport on Selected Date',
			description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Urna, tortor tempus.',
			bg: 'bg-[#006380]'
		}
	];
</script>

<section class="flex flex-col items-center justify-between gap-10 px-4 py-16 md:flex-row md:px-12">
	<!-- Steps -->
	<div class="flex-1 md:pr-10">
		<h3 class="mb-6 text-sm font-bold text-[#666] uppercase">Easy and Fast</h3>
		<h2 class="mb-8 font-serif text-[2.5rem] leading-snug font-bold text-[#181E4B]">
			Book Your Next Trip<br />In 3 Easy Steps
		</h2>

		<ul>
			{#each steps as step}
				<li class="mb-6 flex items-start">
					<span
						class={`h-[50px] w-[55px] ${step.bg} mr-4 flex items-center justify-center rounded-[30%] text-lg text-white`}
					>
						<i class={`fa-solid ${step.icon}`}></i>
					</span>
					<div class="text-left text-[#5E6282]">
						<p class="mb-1 font-bold">{step.title}</p>
						<p class="text-sm font-normal">{step.description}</p>
					</div>
				</li>
			{/each}
		</ul>
	</div>

	<!-- Trip Card -->
	<div class="relative w-[350px] rounded-xl bg-white p-4 shadow-lg">
		<img src="/assets/imgs/Rectangle 17.jpg" alt="Trip to Greece" class="w-full rounded-lg" />

		<!-- Mini Card -->
		<div
			class="absolute -right-[90px] bottom-[60px] z-10 flex w-[260px] items-center rounded-xl bg-white px-4 py-2 shadow-md"
		>
			<img
				src="/assets/imgs/image 33.png"
				alt="Trip to Rome"
				class="mr-3 h-[50px] w-[50px] rounded-full"
			/>
			<div class="flex flex-col gap-1 text-left text-black">
				<p class="text-xs text-[#84829A]">Ongoing</p>
				<p class="text-sm font-medium">Trip to Rome</p>
				<p class="text-[0.75rem] text-[#84829A]">
					<span class="font-semibold text-[#8A79DF]">40%</span> completed
				</p>
				<div class="h-[5px] w-full overflow-hidden rounded bg-gray-300">
					<div class="h-full w-[40%] bg-[#8A79DF]"></div>
				</div>
			</div>
		</div>

		<!-- Card Content -->
		<div class="pt-4 text-left">
			<h3 class="text-lg font-semibold text-black">Trip To Greece</h3>
			<p class="mb-2 text-sm text-[#84829A]">14-29 June | by Robbin jr</p>
			<div class="mb-4 flex gap-3">
				<div
					class="flex h-10 w-10 items-center justify-center rounded-full bg-gray-100 text-[#84829A]"
				>
					<i class="fa-solid fa-leaf"></i>
				</div>
				<div
					class="flex h-10 w-10 items-center justify-center rounded-full bg-gray-100 text-[#84829A]"
				>
					<i class="fa-solid fa-map"></i>
				</div>
				<div
					class="flex h-10 w-10 items-center justify-center rounded-full bg-gray-100 text-[#84829A]"
				>
					<i class="fa-solid fa-paper-plane"></i>
				</div>
			</div>
			<div class="flex items-center justify-between">
				<p class="text-sm text-[#84829A]">
					<i class="fa-solid fa-building mr-2"></i>24 people going
				</p>
				<i class="fa-regular fa-heart text-lg text-[#4152CA]"></i>
			</div>
		</div>

		<!-- Background Glow -->
		<div
			class="absolute -top-[60px] -right-[40px] -z-10 h-full w-full rounded-full bg-[#59b1e633] blur-[40px]"
		></div>
	</div>
</section>
