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
		<p>An OS conceived for CTF competitions</p>

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
	<h2>What is CTFcap?<br>
		What's the difference between CTFcap and other OS?</h2>
	<p>CTFcap is a OS made to have all the tools you need for CTF competitions.<br>
	It is lightweight, fast, and easy to use. Unlike other OS, CTFcap is specifically designed for CTFs, with a focus on usability and performance.
	</p>
</section>

<section class="get-started">
	<div class="gs-inner">
		<h2>Get started</h2>
		<p class="lead">Ready to explore?<br>
			Go here to have the "Get started" guide.</p>
		<a class="btn-cta" href="/docs" aria-disabled="true">
			Coming soon — Get started
		</a>
	</div>
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

		.get-started {
		margin: 2rem 0;
		display: flex;
		justify-content: center;
	}
	.get-started .gs-inner {
		background: rgba(0,0,0,0.03);
		border: 1px dashed rgba(0,0,0,0.1);
		padding: 1.25rem 1.5rem;
		border-radius: 8px;
		text-align: center;
		max-width: 42rem;
		width: 100%;
	}
	.get-started h2 {
		margin: 0 0 0.5rem 0;
		font-size: 1.25rem;
	}
	.get-started .lead {
		margin: 0 0 1rem 0;
		color: var(--color-text);
	}
	.btn-cta {
		display: inline-block;
		padding: 0.5rem 1rem;
		background: transparent;
		border: 1px solid rgba(0,0,0,0.12);
		border-radius: 6px;
		color: var(--color-text);
		text-decoration: none;
		font-weight: 700;
		font-size: 0.9rem;
		cursor: not-allowed;
		opacity: 0.85;
	}
	.btn-cta {
		cursor: pointer;
		opacity: 1;
	}

/* Dark Mode */
:root {
	--color-theme-1: #4db3ff; /* accent light blue */
	--color-theme-2: #1e81d3; /* secondary blue */
	--color-text: rgba(255, 255, 255, 0.9);
	--color-bg-dark: #0a1523; /* dark navy background */
	--color-surface-dark: #102842; /* panels / cards */
	--color-hover: #2d91e8;
}

/* Base dark background */
:global([data-theme='dark'] body) {
	background-color: var(--color-bg-dark);
	color: var(--color-text);
}

/* Main title section */
:global([data-theme='dark']) .main h1 {
	color: var(--color-theme-1);
}

:global([data-theme='dark']) .main h2 {
	color: var(--color-theme-2);
}

/* Make text readable */
:global([data-theme='dark'] .main p),
:global([data-theme='dark'] p) {
	color: rgba(235, 245, 255, 0.9); /* brighter, soft white-blue */
}

/* Fix the Info box */
:global([data-theme='dark']) .Infos {
	background-color: var(--color-surface-dark);
	color: var(--color-text);
	box-shadow: 0 2px 10px rgba(0, 0, 0, 0.4);
	border: 1px solid rgba(255, 255, 255, 0.05);
}

:global([data-theme='dark']) .Infos h2 {
	color: var(--color-theme-1);
}

/* Buttons */
:global([data-theme='dark']) button {
	background-color: var(--color-theme-2);
	color: white;
}

:global([data-theme='dark']) button:hover {
	background-color: var(--color-theme-1);
	transform: translateY(-3px);
	box-shadow: 0 8px 16px rgba(0, 0, 0, 0.25);
}

:global([data-theme='dark']) button a {
	color: white;
	text-decoration: none;
}

/* Get started card */
:global([data-theme='dark']) .get-started .gs-inner {
	background: rgba(255, 255, 255, 0.05);
	border: 1px dashed rgba(255, 255, 255, 0.1);
}

:global([data-theme='dark']) .btn-cta {
	border-color: rgba(255, 255, 255, 0.2);
	color: var(--color-theme-1);
}

:global([data-theme='dark']) .btn-cta:hover {
	border-color: var(--color-theme-1);
	background: rgba(77, 179, 255, 0.1);
}

/* Images */
:global([data-theme='dark']) .image-content img {
	filter: brightness(0.95) contrast(1.1);
}

/* Smooth transitions */
:global(body),
:global(button),
:global(a),
:global(.Infos),
:global(.gs-inner) {
	transition: background-color 0.3s ease, color 0.3s ease, border-color 0.3s ease;
}
</style>
