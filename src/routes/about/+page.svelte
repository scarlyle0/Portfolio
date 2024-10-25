<svelte:head>
	<title>Sean Carlyle — About</title>
</svelte:head>

<div>
	<main>
		<h1>About</h1>
		<p>
			I recently graduated from the University of California, Santa Cruz, with a degree in Computer Science.
			My journey into technology began with a fascination for video games and how they worked, which ultimately led me to pursue a career in software development.
			I found a passion for building software that invites interaction and brings enjoyment to others.
			Through my job and personal projects, I have gained valuable experience in languages like JavaScript and Python, but I am always looking to improve.
		</p>
		<p>
			I also have a passion for game development and really enjoy the creative challenge.
			I am currently seeking opportunities to improve my craft and work on important projects that foster collaboration and encourage continuous learning.
		</p>
	</main>

	<div>
		<img src='background.png' alt="pixel-artwork" id="background-image">
	</div>
</div>

<style>
	div {
		display: flex;
		flex-direction: column;
		height: 100%; 
		justify-content: flex-start; 
	}

	main {
		padding: 20px;
	}

	#background-image {
		image-rendering: pixelated;
	}

	@media (min-width: 900px) {
		main > h1 {
			font-size: 48px;
		}
	}
</style>