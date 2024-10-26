<script lang="ts">
	interface Project {
		title: string;
		description: string;
		status: string;
		logo: string;
		link?: string;
	}

	const projects: Project[] = [
		{
			title: 'TrackNow',
			description: 'A social media feed focusing on simracing and motorsports.',
			status: 'In Development',
			logo: 'src/img/2.png',
			link: 'https://github.com/vantage-ola/tracknow'
		},
		{
			title: 'TrackNow Pro',
			description: 'TrackNow, but with enhanced features for a premium experience.',
			status: 'Planning',
			logo: 'src/img/3.png'
		},
		{
			title: 'The Weather Render',
			description:
				'A software that fetches real-time weather data and integrates it into sim racing platforms for an authentic experience.',
			status: 'Concept',
			logo: 'src/img/1.png'
		}
	];
</script>

<section class="py-24 md:py-32">
	<div class="container mx-auto px-4">
		<h2 class="text-5xl font-bold text-center mb-16">Projects</h2>
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12">
			{#each projects as project (project.title)}
				{#if project.link}
					<a
						href={project.link}
						target="_blank"
						rel="noopener noreferrer"
						class="group bg-white rounded-xl shadow-lg overflow-hidden hover:bg-gray-100 hover:shadow-2xl transition duration-300"
					>
						<div class="p-6 flex flex-col items-center text-center transition-transform group-hover:scale-105 duration-300">
							<img src={project.logo} alt={project.title + ' logo'} class="w-16 h-16 mb-4 object-contain" />
							<h3 class="text-2xl font-semibold mb-3 group-hover:text-yellow-400 transition-colors duration-300">
								{project.title}
							</h3>
							<p class="text-gray-600 mb-4">{project.description}</p>
							<span
								class="inline-block bg-green-100 text-green-800 text-sm font-semibold px-3 py-1 rounded-full group-hover:bg-green-200"
							>
								{project.status}
							</span>
						</div>
					</a>
				{:else}
					<div class="bg-white rounded-xl shadow-lg overflow-hidden p-6 flex flex-col items-center text-center hover:bg-gray-100 hover:shadow-2xl transition duration-300">
						<img src={project.logo} alt={project.title + ' logo'} class="w-16 h-16 mb-4 object-contain" />
						<h3 class="text-2xl font-semibold mb-3 hover:text-yellow-400 transition-colors duration-300">
							{project.title}
						</h3>
						<p class="text-gray-600 mb-4">{project.description}</p>
						<span
							class="inline-block bg-green-100 text-green-800 text-sm font-semibold px-3 py-1 rounded-full hover:bg-green-200"
						>
							{project.status}
						</span>
					</div>
				{/if}
			{/each}
		</div>
	</div>
</section>

