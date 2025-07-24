<script>
	function handleSubmit(event) {
		event.preventDefault();

		alert('Subscribed!');
	}
</script>

<section
	class="relative my-24 max-h-[600px] rounded-[120px_15px_15px_15px] bg-[#dfd7f985] px-8 py-12 text-center sm:rounded-[60px_10px_10px_10px] sm:px-4 sm:py-8 md:px-8 md:py-12"
>
	<!-- Background Circles -->
	<img
		src="/assets/imgs/Group 42.png"
		class="pointer-events-none absolute bottom-0 left-[10px] opacity-30 sm:h-[200px] sm:w-[150px]"
		alt="Decore"
	/>
	<img
		src="/assets/imgs/Group 590.png"
		class="pointer-events-none absolute top-0 right-0 opacity-30"
		alt="Decore"
	/>

	<!-- Title -->
	<h2 class="mb-20 text-3xl leading-[2] font-semibold text-[#3f3d56] sm:mb-12 sm:text-[1.7rem]">
		Subscribe to get information, latest news and other <br />
		interesting offers about <strong>Jadoo</strong>
	</h2>

	<!-- Subscribe Form -->
	<form
		class="flex flex-wrap items-center justify-center gap-4 sm:flex-col md:flex-col"
		onsubmit={handleSubmit}
	>
		<div class="relative  w-[400px] sm:max-w-none">
			<i class="fas fa-envelope absolute top-1/2 left-3 -translate-y-1/2 text-[#39425D]"></i>
			<input
				type="email"
				placeholder="Your email"
				required
				class="placeholder-opacity-100 box-border w-full rounded-lg border-none py-3 pr-4 pl-10 text-base placeholder-[#39425D] outline-none "
			/>
		</div>
		<button
			type="submit"
			class="cursor-pointer rounded-lg border-none bg-[#FF946D] px-6 py-3 text-base text-white transition-opacity duration-300 hover:opacity-90"
		>
			Subscribe
		</button>
	</form>

	<!-- Fly Icon -->
	<div
		class="absolute top-0 right-0 z-10 flex h-[50px] w-[50px] translate-x-1/2 -translate-y-1/2 items-center justify-center rounded-full bg-[#5f58f5] text-[1.25rem] text-white sm:top-2.5 sm:right-2.5 sm:h-[40px] sm:w-[40px] sm:translate-x-0 sm:-translate-y-0 sm:text-base md:top-3 md:right-3"
	>
		<i class="fas fa-paper-plane"></i>
	</div>
</section>
