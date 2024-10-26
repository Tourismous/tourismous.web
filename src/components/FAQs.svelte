<script>
	// @ts-nocheck

	import SectionWrapper from './SectionWrapper.svelte';
	let faqs = [
		{
			question: 'What is Tourismous?',
			ans: 'Tourismous is a small team of developers building racing-related software.'
		},
		{
			question: 'Is the software open source or closed source?',
			ans: 'We build both open source and closed source projects.'
		},
		{
			question: 'How do I join the team?',
			ans: "You can fill out a form indicating some personal details and your experience in the 'Team' section of this website. We will contact you shortly."
		},
		{
			question: 'If I join the team, will I get paid?',
			ans: 'No. Unfortunately, this is a small team started by a young Nigerian guy who loves simracing and motorsports. Right now, there is no money made, but hopefully in the near future when we start to make money from the products we develop. Consider it as a hobby you do on the weekends.'
		},
		{
			question: 'I am not a technical person. Can I still join?',
			ans: 'Yes, we also need people who are good with social media and other relevant departments.'
		},
		{
			question: 'What kind of projects do you work on?',
			ans: 'We work on a variety of racing-related software projects, including simracing tools, data analysis platforms, and more.'
		},
		{
			question: 'How can I support Tourismous?',
			ans: 'You can support us by spreading the word, contributing to our open source projects, or donating to help us continue our work.'
		},
		{
			question: 'Do you offer any training or resources for new team members?',
			ans: 'Yes, we provide resources and training to help new team members get up to speed with our projects and technologies.'
		},
		{
			question: 'What is the future vision for Tourismous?',
			ans: 'Our future vision is to become a leading provider of innovative racing-related software, contributing to the growth and enjoyment of the motorsports community.'
		}
	];
</script>

<SectionWrapper id="faqs">
	<div class="flex flex-col gap-10 sm:gap-14 md:gap-24 py-20 flex-1 items-center justify-center">
		<div class="flex flex-col gap-2">
			<p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
				For all your questions, qualms & queries
			</p>
			<h3
				class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center"
			>
				Frequently Asked Questions
			</h3>
		</div>
		<div class="flex flex-col gap-8 sm:gap-10 md:gap-14 w-full">
			{#each faqs as faq}
				<div class="flex flex-col gap-2 text-left max-w-[800px] w-full mx-auto relative p-4 px-6">
					<div class="absolute top-0 left-0 w-1/3 h-[1px] bg-slate-950 -translate-x-4"></div>
					<div class="absolute top-0 left-0 h-2/3 w-[1px] bg-slate-950 -translate-y-4"></div>
					<h4 class="text-lg sm:text-xl md:text-2xl pt-2">
						{faq.question}
					</h4>
					<p class="pl-2">{faq.ans}</p>
				</div>
			{/each}
		</div>
	</div>
</SectionWrapper>
