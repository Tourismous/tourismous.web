<script lang="ts">
	interface Project {
		title: string;
		description: string;
		status: string;
		icon: string;
		link?: string;
	}

	const projects: Project[] = [
		{
			title: 'TrackNow',
			description: 'A social media feed focusing on simracing and motorsports.',
			status: 'In Development',
			icon: '🏁',
			link: 'https://github.com/vantage-ola/tracknow'
		},
		{
			title: 'TrackNow pro',
			description: 'tracknow, but better.',
			status: 'Planning',
			icon: '🔧'
		},
		{
			title: 'The Weather Reder',
			description:
				'A software that fetches real-time weather data and seamlessly integrates it into sim racing platforms for an authentic racing experience.',
			status: 'Concept',
			icon: '👥'
			// No link for this project
		}
	];
</script>

<section class="py-24 md:py-32">
	<div class="container mx-auto px-4">
		<h2 class="text-5xl font-semibold text-center mb-16">Our Projects</h2>
		<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
			{#each projects as project (project.title)}
				{#if project.link}
					<a
						href={project.link}
						target="_blank"
						rel="noopener noreferrer"
						class="block bg-white rounded-lg shadow-md p-6 transition-transform hover:scale-105 cursor-pointer"
					>
						<div class="text-4xl mb-4">{project.icon}</div>
						<h3 class="text-xl font-semibold mb-2">{project.title}</h3>
						<p class="text-gray-600 mb-4">{project.description}</p>
						<span
							class="inline-block bg-blue-100 text-blue-800 text-sm font-semibold px-2 py-1 rounded"
						>
							{project.status}
						</span>
					</a>
				{:else}
					<div class="bg-white rounded-lg shadow-md p-6 transition-transform hover:scale-105">
						<div class="text-4xl mb-4">{project.icon}</div>
						<h3 class="text-xl font-semibold mb-2">{project.title}</h3>
						<p class="text-gray-600 mb-4">{project.description}</p>
						<span
							class="inline-block bg-blue-100 text-blue-800 text-sm font-semibold px-2 py-1 rounded"
						>
							{project.status}
						</span>
					</div>
				{/if}
			{/each}
		</div>
	</div>
</section>
