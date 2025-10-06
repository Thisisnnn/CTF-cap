<script lang="ts">
	import Github from '$lib/images/Github.svg';
</script>

<svelte:head>
	<title>CTF Cap</title>
	<meta name="CTFcap" content="OS léger pour les CTFs" />
</svelte:head>

<section class="main">
	<div class="text-content">
		<h1>CTF</h1>
		<h2>cap</h2>
		<p>Un OS léger pour les CTFs</p>

		<div class="buttons">
			<button><a href="/Documentation">Documentation</a></button>
			<button><a href="/download">Download</a></button>
		</div>
	</div>

	<div class="image-content">
		<img src={Github} alt="GitHub logo" />
	</div>
</section>

<section class="Infos">
	<h2>Pourquoi CTFcap?</h2>
	<p>CTFcap est conçu pour être un système d'exploitation léger et efficace, spécialement adapté aux besoins des compétitions de Capture The Flag (CTF). Il offre un environnement sécurisé et optimisé pour les participants, avec des outils préinstallés et une interface utilisateur intuitive.</p>
</section>



<style>
	.main {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
	margin-top: 80px;
    height: 100vh;        /* make it full viewport height */
    box-sizing: border-box;
}


	.text-content {
		display: flex;
		flex-direction: column;
		align-items: flex-start;
	}

	.main h1, .main h2 {
		font-size: 7rem;
		line-height: 1;
		font-weight: 900;
		margin: 0;
	}
	.main h1 {
		color: #104b81;
	}
	.main h2 {
		color: #145ea3;
		margin-left: 100px;
	}

	.Infos h2 {
		font-size: 2.5rem;
		margin-top: 2rem;
		margin-bottom: 1rem;
		margin-left: 30px;
		color: #104b81;
	}

	p {
		font-size: 1.5rem;
		margin-top: 2rem;
		margin-bottom: 2rem;
		margin-left: 30px;
		color: #334155;
	}

	.buttons {
		display: flex;
		gap: 20px;
		margin-top: 20px;
	}

	button {
		background-color: #104b81;
		color: white;
		border: none;
		border-radius: 8px;
		font-size: 1.25rem;
		font-weight: 600;
		padding: 12px 24px;
		cursor: pointer;
		box-shadow: 0 4px 12px rgba(0,0,0,0.2);
		transition: transform 0.2s ease, box-shadow 0.2s ease;
	}
	
	button:hover {
		transform: translateY(-3px);
		box-shadow: 0 8px 16px rgba(0,0,0,0.25);
		background-color: #165fa3;
	}

	.image-content {
		display: flex;
		justify-content: center;
		align-items: center;
		flex: 1;
		margin-left: 200px;
	}

	.image-content img {
		width: 100%;
		max-width: 35;
	}

	.Infos
	{
		margin-top: 0;
		margin-bottom: 50px;
		border-radius: 15px;
		background-color: #e6f1fa;
		padding: 20px;
	}
</style>
