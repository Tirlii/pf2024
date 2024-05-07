<script>
	import Header from './Header.svelte';
	import './styles.css';
	import Intro from './Intro/Intro.svelte';
	import Projects from './components/projectList.svelte'
</script>

<div class="app">
	<Header />

	<Intro />
	<Projects />

	<footer>
		<p>visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</p>
	</footer>
</div>

<style>

@font-face {
	font-family: 'CabinetGrotesk';
	src: url('../lib/fonts/CabinetGrotesk-Variable.woff2') format('woff2'),
		url('../lib/fonts/CabinetGrotesk-Variable.woff') format('woff'),
		url('../lib/fonts/CabinetGrotesk-Variable.ttf') format('truetype');
	font-weight: 100 900;
	font-display: swap;
	font-style: normal;
}



	.app {
		display: flex;
		flex-direction: column;
		font-family:'CabinetGrotesk';
	}


	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
