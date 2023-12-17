<script>
	import { createBackgroundAnimation } from '../functions/createBackgroundAnimation';
	import { onMount } from 'svelte';
	onMount(() => {
		createBackgroundAnimation();
	});
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Anton Khantelev website" />
	<style>
		header nav a {
			color: var(--color-text-dark);
		}
	</style>
</svelte:head>

<section class="wrapper">
	<div class="blur" />
	<div class="blur" />
	<div class="blur" />
	<h1>Anton Khantelev</h1>
	<h2>Front-end developer</h2>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1,
	h2 {
		color: var(--color-text-dark);
		text-transform: uppercase;
		margin: 2rem 0;
		margin: 0 auto;
		text-align: center;
		z-index: 2;
		position: relative;
		width: 100%;
	}

	h1 {
		font-size: 6vw;
		font-weight: 800;
	}

	h2 {
		font-size: 2vw;
	}

	:root {
		--color-bg: #ecd5b8;
		--blur-1-size: clamp(400px, 60vw, 60vw);
		--blur-2-size: clamp(300px, 40vw, 40vw);
		--blur-3-size: clamp(100px, 10vw, 10vw);
		--blur-amount: clamp(40px, 5vw, 90px);
	}

	.blur {
		position: absolute;
		z-index: 1;
		border-radius: 900px;
		filter: blur(var(--blur-amount));
		background: var(--color-bg);
	}

	.blur:nth-child(1) {
		height: var(--blur-1-size);
		width: calc(var(--blur-1-size) * 1.1);
	}

	.blur:nth-child(2) {
		filter: blur(var(--blur-amount)) hue-rotate(135deg) brightness(1.3);
		height: var(--blur-2-size);
		width: calc(var(--blur-2-size) * 0.75);
		top: 20vh;
		right: 20vh;
	}

	.blur:nth-child(3) {
		filter: blur(var(--blur-amount)) hue-rotate(-135deg);
		height: var(--blur-3-size);
		width: calc(var(--blur-3-size) * 2);
		bottom: 20vh;
		left: 20vw;
	}

	section {
		padding: 5vw;
		height: 100vh;
		background: #f4f4f4;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		position: relative;
		overflow: hidden;
	}

	* {
		box-sizing: border-box;
	}
</style>
