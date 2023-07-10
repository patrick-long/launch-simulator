<script lang="ts">
	import Header from './Header.svelte';
	import './styles.css';
</script>

<div class="app">
	<Header />

	<main>
		<slot />
	</main>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		min-width: 100vw;
		min-height: 100vh;
		display: flex;
		flex-direction: column;
		box-sizing: border-box;
	}
</style>
