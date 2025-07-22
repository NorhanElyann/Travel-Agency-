<script lang="ts">
	import BookTripSection from '$lib/sections/BookTrip/BookTripSection.svelte';
	import FooterSection from '$lib/sections/Footer/FooterSection.svelte';
	import HeaderSection from '$lib/sections/Header/HeaderSection.svelte';
	import HeroSection from '$lib/sections/Hero/HeroSection.svelte';
	import PartnersSection from '$lib/sections/Partners/PartnersSection.svelte';
	import ScrollToTop from '$lib/sections/ScrollToTop/ScrollToTop.svelte';
	import ServicesSection from '$lib/sections/Services/ServicesSection.svelte';
	import SubscribeSection from '$lib/sections/Subscribe/SubscribeSection.svelte';
	import TestimonialsSection from '$lib/sections/Testimonials/TestimonialsSection.svelte';
	import TopSellingSection from '$lib/sections/TopSelling/TopSellingSection.svelte';
</script>



<main class="relative  text-[#5E6282]">
    <div
	class="absolute top-0 right-0 z-[-1] h-[650px] w-[1000px] bg-[url('/assets/imgs/Decore.png')] bg-contain bg-right-top bg-no-repeat"
    ></div>
    
	<section class="relative z-10 container mx-auto px-5 pb-10 pt-10 md:px-30">
		<HeaderSection />
        <HeroSection />
        <ServicesSection />
        <TopSellingSection/>
        <BookTripSection/>
        <TestimonialsSection/>
        <PartnersSection/>
        <SubscribeSection/>
        <FooterSection/>
        <ScrollToTop/>
	</section>
	

	

</main>
