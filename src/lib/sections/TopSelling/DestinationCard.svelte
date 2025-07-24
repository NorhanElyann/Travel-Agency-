<script >
	let {alt,country,price,duration,src} = $props();
</script>

<div
	class="destination-card relative h-[460px] w-[350px] overflow-hidden rounded-[24px] shadow-lg transition hover:-translate-y-1 hover:shadow-xl"
>
	<img {src} {alt} class="block h-full w-full object-cover" />
	<div class="overlay-text absolute bottom-0 h-1/4 w-full bg-white p-4 text-[#5E6282]">
		<div class="top-line mb-5 flex items-center justify-between">
			<p>{alt}{country && `, ${country}`}</p>
			<span class="price">{price}</span>
		</div>
		<div class="duration text-left text-sm font-normal">
			<i class="fa-solid fa-paper-plane mr-2 text-[0.95rem] text-black"></i>
			{duration}
		</div>
	</div>
</div>
