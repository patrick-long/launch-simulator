<script>
	import { page } from '$app/stores';
	import github from '$lib/images/github.svg';

	$: path = $page.url.pathname;
</script>

<header>
	<div class="corner" />

	<nav class="nav-container">
		<ul class="route-options">
			<li class="route-option">
				<a
					class="route-option-link
						{path === '/' || path === '' ? 'selected' : ''}
					"
					href="/"
				>
					Home
				</a>
			</li>
			<li class="route-option">
				<a
					class="route-option-link
						{path === '/simulator' ? 'selected' : ''}
					"
					href="/simulator"
				>
					Simulator
				</a>
			</li>
			<li class="route-option">
				<a
					class="route-option-link
						{path === '/about' ? 'selected' : ''}
					"
					href="/about"
				>
					About
				</a>
			</li>
		</ul>
	</nav>

	<div class="corner">
		<a target="_blank" href="https://github.com/patrick-long/launch-simulator">
			<img src={github} alt="GitHub" />
		</a>
	</div>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		position: fixed;
		width: 100%;
	}

	.corner {
		width: 4rem;
		height: 4rem;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	.corner img {
		width: 3rem;
		height: 3rem;
		object-fit: contain;
	}

	.nav-container {
		display: flex;
		justify-content: center;
		height: 3rem;
	}

	.route-options {
		padding: 0;
		margin: 0;
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 1rem;
		list-style: none;
	}

	.route-option {
		display: flex;
		align-items: center;
		position: relative;
		height: 100%;
	}

	.route-option-link {
		color: var(--color-text);
		font-weight: 500;
		font-size: 1.25rem;
		text-transform: uppercase;
		letter-spacing: 0.25rem;
		text-indent: 0.25rem;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	.route-option-link.selected,
	.route-option-link:hover {
		color: var(--color-theme-1);
	}

	.route-option-link::after {
		content: '';
		height: 1px;
		width: 75%;
		background-color: var(--color-theme-1);
		position: absolute;
		top: 90%;
		right: 12.5%;
		opacity: 0;
		transition: opacity 0.2s linear;
	}

	.route-option-link.selected::after,
	.route-option-link:hover::after {
		opacity: 1;
	}
</style>
