<script>
	import * as Fluent from "fluent-svelte";
	import "fluent-svelte/theme.css";
	import { base } from '$app/paths';
</script>

<style>

	nav {
		display: flex;
		justify-content: left;
		align-items: center;
		padding: 8px;
	}

	h1, h2, h3, h4, h5, h6, span, p, nav a {
		font-family: 'Segoe UI', system-ui, -apple-system, BlinkMacSystemFont, Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
	}

	h1 {
		font-weight: 500;
		transition: 1s ease-in-out;
		animation: ease-in-out font-weight;
	}

	nav {
		background: var(--fds-solid-background-base);
		border-bottom: 1px solid rgba(205, 205, 205, 0.25);
	}

	nav a {
		text-decoration: none;
		color: white;
		margin-right: 14px;
	}

	nav a.logo img {
		width: 30px;
		height: 30px;
		border-radius: 100%;
		margin-top: 5px;
		margin-left: 5px;
		margin-right: 5px;
	}

	main {
		display: block;
		padding: 85px 65px;
	}

	main * {
		display: block;
	}

	main h1, main h2 {
		margin-top: 0;
	}

	footer {
		padding-top: 10px;
		padding-bottom: 10px;
		padding-left: 25px;
		background: var(--fds-solid-background-base);
		border-top: 1px solid rgba(205, 205, 205, 0.25);
		display: flex;
		flex-direction: column;
		align-items: flex-start;
		position: absolute;
		bottom: 0;
		width: calc(100vw - 25px);
	}

	@keyframes font-weight {
		0% {
			font-weight: 500;
		}
		25% {
			font-weight: 600;
		}
		100% {
			font-weight: 700;
		}
	}
</style>

<div>
	<nav>
		<a href="/" class="logo"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6f/Android_11_Developer_Preview_logo.svg/2048px-Android_11_Developer_Preview_logo.svg.png" alt="rvc11's pfp"></a>
		<Fluent.Button href="{base}/" style="margin-right: 14px;" variant="hyperlink">Home</Fluent.Button>
		<Fluent.Button href="{base}/plans" style="margin-right: 14px;" variant="hyperlink">Plans</Fluent.Button>
		<Fluent.Button href="{base}/contact">Contact me</Fluent.Button>
	</nav>
	<main>
		<h1>Contact me</h1>
		<p>You can contact me on these:</p>
        	<Fluent.Button onClick="window.open('https://twitter.com/PrelevatedIns', '_blank')">Twitter</Fluent.Button>
		<Fluent.Button onClick="window.open('mailto:membermadde.insiddev25120@hotmail.com', '_blank')">Hotmail</Fluent.Button>
		<Fluent.Button onClick="window.open('https://github.com/redvelvetcake11', '_blank')">GitHub</Fluent.Button>
		<Fluent.Button onClick="window.open('https://app.revolt.chat/swzkRmn0', '_blank')">Revolt</Fluent.Button>
	</main>
	<footer>
		<h5 style="margin: 0px; margin-top: 10px">Powered by:</h5>
		<Fluent.Button href="https://kit.svelte.dev" variant="hyperlink" style="margin-top: 10px; margin-bottom: 10px">SvelteKit</Fluent.Button>
		<Fluent.Button href="https://fluent-svelte.vercel.app/" variant="hyperlink" style="margin-bottom: 10px">Fluent Svelte</Fluent.Button>
		<h5 style="margin: 0px; margin-bottom: 10px">Made and contributed by:</h5>
                <Fluent.Button href="/" variant="hyperlink" style="margin-bottom: 10px">RedVelvetCake11</Fluent.Button>
	</footer>
</div>
