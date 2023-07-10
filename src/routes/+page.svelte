<svelte:head>
	<title>Launch Simulator</title>
	<meta name="description" content="Rocket launch simulator" />
</svelte:head>

<section class="main-section" />

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	.main-section {
		display: flex;
		flex: 1;
		height: 100%;
		width: 100%;
		background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0.25), rgba(0, 0, 0, 0.75)),
			url('$lib/images/launch.jpg');
		/* filter: blur(3px); */
		-webkit-background-size: cover;
		-moz-background-size: cover;
		-o-background-size: cover;
		background-size: cover;
	}
</style>
