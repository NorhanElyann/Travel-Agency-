<script>
	let isVisible = $state(false);

	const handleScroll = () => (isVisible = window.scrollY > 200);

	const scrollToTop = () =>
		window.scrollTo({
			top: 0,
			behavior: 'smooth'
		});
</script>

<svelte:window onscroll={handleScroll} />

<!-- svelte-ignore a11y_consider_explicit_label -->
<button
	onclick={scrollToTop}
	class:hidden={!isVisible}
	class=" fixed right-[30px] bottom-[30px] z-[999] cursor-pointer rounded-full bg-[#DF6951] p-3 text-lg text-white transition-colors duration-300 hover:bg-[#c05340]"
	title="Go to top"
>
	<i class="fas fa-arrow-up"></i>
</button>
