<script>
	import skills from '$lib/Skills';
	import experiences from '$lib/Experiences';
</script>

<svelte:head>
	<title>Gavyn Ezell — About</title>
</svelte:head>

<div class="container">
	<main>
		<h2>Skills</h2>
		{#each Object.entries(skills) as [section, technologies]}
			<ul>
				<li>
					<h3>{section}:</h3>
					<div class="list">
						{#each technologies as technology}
							<div class="greytext">
								{technology}
							</div>
						{/each}
					</div>
				</li>
			</ul>
		{/each}
		
		<h2>Experience</h2>
		{#each experiences as exp}
			<ul>
				<li>
					<h3>
						{exp.company} - {exp.title}
					</h3>
					<h4>{exp.duration}</h4>
					<ul class="greytext">
						{#each exp.description as bullet}
						<li>
							{bullet}
						</li>
						{/each}
					</ul>
				</li>
			</ul>
		{/each}
	</main>
</div>

<style>
	.greytext {
		color: #708090;
	}

	.container {
		max-width: 900px;
		padding: 0;
		display: flex;
		justify-content: center;
	}

	main {
		max-width: 100%;
		min-height: 500px;
		text-align: left;
		margin: 0 auto;
		box-sizing: border-box;
		margin-bottom: 100px;
	}

	h2 {
		margin-top: 50px;
	}

	.list {
		display: flex;
		flex-direction: row;
		gap: 30px;
	}

	@media (max-width: 600px) {
		.list {
			flex-direction: row;
			flex-wrap: wrap;
		}
	}
</style>