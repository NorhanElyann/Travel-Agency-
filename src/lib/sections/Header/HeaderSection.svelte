<script lang="ts">
	let navOpen = false;

	function toggleMenu() {
		navOpen = !navOpen;
	}
</script>

<header class="relative z-50 flex items-center justify-between py-4 text-black">
	<div class="logo">
		<img src="/assets/imgs/Logo.svg" alt="Jadoo Logo" class="h-auto max-w-full" />
	</div>

	<nav class="hidden items-center gap-6 md:flex">
		<a href="#" class="text-[17px] font-medium hover:text-[#DF6951]">Destinations</a>
		<a href="#" class="text-[17px] font-medium hover:text-[#DF6951]">Hotels</a>
		<a href="#" class="text-[17px] font-medium hover:text-[#DF6951]">Flights</a>
		<a href="#" class="text-[17px] font-medium hover:text-[#DF6951]">Bookings</a>
		<a href="#" class="text-[17px] font-medium hover:text-[#DF6951]">Login</a>
		<a
			href="#"
			class="rounded border border-black px-4 py-1 text-[17px] font-medium hover:text-[#DF6951]"
			>Sign up</a
		>
		<select class="ml-4 bg-transparent text-[15px] font-medium focus:outline-none">
			<option value="en">EN</option>
		</select>
	</nav>

	<!-- Menu toggle icon for mobile -->
	<div class="cursor-pointer text-2xl md:hidden" on:click={toggleMenu}>
		<i class="fas fa-bars"></i>
	</div>

	<!-- Mobile menu -->
	{#if navOpen}
		<nav
			class="absolute top-[70px] right-5 z-50 flex flex-col gap-4 rounded-lg bg-white p-4 shadow-lg"
		>
			<a href="#">Destinations</a>
			<a href="#">Hotels</a>
			<a href="#">Flights</a>
			<a href="#">Bookings</a>
			<a href="#">Login</a>
			<a href="#" class="rounded border border-black px-4 py-1">Sign up</a>
			<select class="bg-transparent text-[15px] font-medium focus:outline-none">
				<option value="en">EN</option>
			</select>
		</nav>
	{/if}
</header>
