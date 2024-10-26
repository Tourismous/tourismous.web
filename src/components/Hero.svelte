<script>
	// @ts-nocheck

	import CtAs from './CTAs.svelte';
	import Header from './Header.svelte';
	import SectionWrapper from './SectionWrapper.svelte';
	import Project from './Project.svelte';
</script>

<SectionWrapper>
	<Header />
	<div class="flex flex-col gap-16 flex-1 items-center justify-center">
		<h2
			class="text-6xl sm:text-7xl md:text-8xl lg:text-9xl max-w-[1200px] mx-auto w-full text-center font-bold"
		>
			<span>touris</span><span class="text-yellow-300">mous</span>
		</h2>
		<p class="text-lg sm:text-xl md:text-2xl text-center max-w-[800px] mx-auto w-full">
			A team of devs building racing related software. We aim to provide applications, tools, data
			analytics, and community support to enhance your racing experience.
		</p>
		<CtAs />
	</div>

</SectionWrapper>
