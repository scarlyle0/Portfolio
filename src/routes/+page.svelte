<script>
	import FaLinkedin from 'svelte-icons/fa/FaLinkedin.svelte';
	import FaGithub from 'svelte-icons/fa/FaGithub.svelte';
	import FaEnvelope from 'svelte-icons/fa/FaEnvelope.svelte';
	import FaFile from 'svelte-icons/fa/FaFile.svelte';
	import { modalOpened } from '$lib/store';
	import SkillExpList from '$lib/components/SkillExpList.svelte';
</script>

<svelte:head>
	<title>Sean Carlyle - Main page</title>
</svelte:head>
<main>
	<div id = "intro">
		<img src="portrait.jpg" alt="pfp">
		<div>
			<h1>Sean Carlyle</h1>
			<h2>Software Developer</h2>
		</div>
	</div>
	<div class="icons">
		<div
			role="button"
			tabindex="0"
			on:keypress={() => {
				modalOpened.set(true);
			}}
			on:click={() => {
				modalOpened.set(true);
			}}
		>
			<div class="icon">
				<FaEnvelope />
			</div>
		</div>

		<a
			href="https://github.com/scarlyle0"
			aria-label="GitHub"
			target="_blank"
			rel="noopener noreferrer"
		>
			<div class="icon">
				<FaGithub />
			</div>
		</a>
		<a
			href="https://www.linkedin.com/in/sean-carlyle/"
			aria-label="Linkedin"
			target="_blank"
			rel="noopener noreferrer"
		>
			<div class="icon">
				<FaLinkedin />
			</div>
		</a>
		<a
		href="SeanCarlyleResume.pdf"
		aria-label="resume"
		target="_blank"
		rel="noopener noreferrer"
	>
		<div style="transform: scale(0.7)"class="icon">
			<FaFile />
		</div>
	</a>
	</div>

	<SkillExpList></SkillExpList>

</main>

<style>
	
	#intro {
		display:flex;
		flex-direction: row;
		align-items: center;
		justify-content: space-between;
		gap: 50px;
		padding-top: 60px;
	}

	a {
		color: white;
		text-decoration: none;
	}
	main {
		text-align: center;
		padding: 0;
		margin: 0 auto;
		text-align: center;

		display: flex;
		flex-direction: column;
		min-height: 100vh;
		justify-content: flex-start;
		align-items: center;
		
	}

	h1 {
		font-weight: 700;
	}

	.icons {
		display: flex !important;
		justify-content: center !important;
		align-items: center;
		gap: 20px;
		cursor: pointer;
		font-size: 30px;
		display: flex;
		justify-content: space-between;
		max-width: 200px;
		margin: 50px auto 0;
	}

	.icon {
		cursor: pointer;
		transition: color 0.2s ease-in-out;
		width: 40px;
	}
	.icon:hover {
		color: #ca3c25;
	}

	@media (min-width: 600px) {
		main {
			max-width: none;
		}
	}

	
	h1 {
		font-weight: 700;
		margin: 0px 0;
	}

	h2 {
		margin: 0;
	}

	img {
		border-radius: 50%;
		width: 256px;
		height: 256px;
	}
</style>
