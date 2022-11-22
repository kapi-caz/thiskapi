<script>
	import '../app.postcss';
	import {
		Footer,
		FooterCopyright,
		FooterLinkGroup,
		FooterBrand,
		FooterLink,
		FooterIcon
	} from 'flowbite-svelte';
	import './styles.css';
</script>

<div class="app">
	<header />

	<main>
		<slot />
	</main>

	<Footer>
		<div class="flex mt-4 space-x-6 sm:justify-center sm:mt-0">
			<FooterIcon href="https://svelte.dev/">
				<img class="w-5 h-5" src="src/lib/images/svelte-logo.svg" alt="Svelte Homepage" />
			</FooterIcon>
			<FooterIcon href="https://flowbite.com">
				<img class="w-5 h-5" src="https://flowbite.com/docs/images/logo.svg" alt="Flowbite" />
			</FooterIcon>
		</div>
	</Footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
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
