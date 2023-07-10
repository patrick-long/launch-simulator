<svelte:head>
	<title>About</title>
	<meta name="description" content="About this app" />
</svelte:head>

<section class="main-content">
	<div class="text-column">
		<h1>About this app</h1>

		<p>
			This is a <a
				class="about-link"
				target="_blank"
				href="https://kit.svelte.dev"
				rel="noopener noreferrer">SvelteKit</a
			> app built for simulating rocket launches with different environmental and engineering factors
			(e.g. wind speed, air resistence, weight, propulsion, etc.).
		</p>
		<p>
			The application was created by <a
				class="about-link"
				href="https://github.com/patrick-long"
				target="_blank"
				rel="noopener noreferrer">Patrick Long</a
			>, with an
			<a
				class="about-link"
				href="https://github.com/patrick-long/launch-simulator-api"
				target="_blank"
				rel="noopener noreferrer">API</a
			> written in C++ to ensure efficient and precise calculations.
		</p>
	</div>
</section>

<style>
	.main-content {
		display: flex;
		flex: 1;
		height: 100%;
		width: 100%;
		background: linear-gradient(to bottom, rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.75)),
			url('$lib/images/about.png');
		background-size: cover;
	}

	.about-link {
		color: var(--color-theme-2);
	}
</style>
