<script lang="ts">
	import { onMount } from 'svelte';

	let isVisible: boolean = false;

	function handleScroll() {
		isVisible = document.body.scrollTop > 200 || document.documentElement.scrollTop > 200;
	}

	function scrollToTop() {
		window.scrollTo({
			top: 0,
			behavior: 'smooth'
		});
	}

	onMount(() => {
		window.addEventListener('scroll', handleScroll);
		return () => window.removeEventListener('scroll', handleScroll);
	});
</script>

<svelte:window onscroll={handleScroll} />

<!-- svelte-ignore a11y_consider_explicit_label -->
<button
	onclick={scrollToTop}
	class="{isVisible
		? 'block'
		: 'hidden'} fixed right-[30px] bottom-[30px] z-[999] cursor-pointer rounded-full bg-[#DF6951] p-3 text-lg text-white transition-colors duration-300 hover:bg-[#c05340]"
	title="Go to top"
>
	<i class="fas fa-arrow-up"></i>
</button>
