<script>
	import { createWordsAnimation } from '../../functions/createWordsAnimation';

	import { onMount } from 'svelte';

	onMount(() => {
		createWordsAnimation();
	});
</script>

<svelte:head>
	<title>Skills</title>
	<meta name="description" content="Skills" />
</svelte:head>

<div class="page">
	<h2>Skills</h2>
	<section class="content">
		<div class="skill-list">
			<div class="skill-box">
				<h3>Main</h3>
				<ul>
					<li>Javascript</li>
					<li>HTML5</li>
					<li>CSS3</li>
					<li>Typescript</li>
					<li>React</li>
					<li>SCSS</li>
					<li>Git</li>
				</ul>
			</div>
			<div class="skill-box">
				<h3>State managers</h3>
				<ul>
					<li>Redux</li>
					<li>Redux-Toolkit</li>
					<li>Effector</li>
				</ul>
			</div>
			<div class="skill-box">
				<h3>Bundlers / tools</h3>
				<ul>
					<li>Webpack</li>
					<li>Rollup</li>
					<li>Gulp</li>
				</ul>
			</div>
			<div class="skill-box">
				<h3>Testing</h3>
				<ul>
					<li>Jest</li>
					<li>Mocha</li>
					<li>Enzyme</li>
					<li>Storybook</li>
					<li>Cypress</li>
				</ul>
			</div>
			<div class="skill-box">
				<h3>Backend</h3>
				<ul>
					<li>Node.js</li>
					<li>Next.js</li>
					<li>MongoDB</li>
					<li>mySQL</li>
				</ul>
			</div>
			<div class="skill-box">
				<h3>Etc</h3>
				<ul>
					<li>GraphQL</li>
					<li>Apollo</li>
					<li>React Native</li>
					<li>Electron.js</li>
					<li>Svelte</li>
					<li>SvelteKit</li>
				</ul>
			</div>
		</div>
		<div class="circle-words">
			<div class="outer">
				<div class="inner">
					Javascript HTML5 CSS3 Typescript React Redux Redux-Toolkit Effector Webpack Gulp Rollup
					Jest Enzyme Mocha Storybook Cypress SASS SCSS BEM Node.js MongoDB mySQL Git GraphQL
					React-Native Electron.js Svelte SvelteKit
				</div>
			</div>
		</div>
	</section>
</div>

<style>
	.page {
		padding-top: var(--header-height);
		font-family: var(--font-mono);
	}

	.content {
		display: flex;
		margin: 0;
		color: black;
		width: 100%
	}

	.circle-words {
		display: flex;
		width: 50%;
		flex-direction: column;
		align-items: center;
		justify-content: start;
	}

	h2 {
		font-size: max(2vw, 20px);
		text-align: center;
		margin-bottom: 0;
		padding-top: 10px;
		font-weight: bold;
	}

	.skill-list {
		display: flex;
		flex-wrap: wrap;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		width: 50%;
		margin: 0;
		height: 100vh;
	}

	.skill-box {
		height: 180px;
		width: 200px;
		padding: 10px;
		display: flex;
		flex-direction: column;
		justify-content: flex-start;
	}

	.skill-box h3 {
		margin: 0;
	}

	.outer {
		position: relative;
		/* position: absolute; */

/* 		top: 50%; */
		top: 20px;
		font: bold 12px sans-serif;
		visibility: hidden;
		margin: 0;
		max-height: 80dvh;
		max-width: 80dvh;
		border: 2px solid #000;
		overflow: hidden;
		box-shadow: -20px 20px 60px #bebebe, 20px -20px 60px #ffffff;
		background: #f8f8f8;
	}

	.inner {
		position: absolute;
		top: 50%;
		left: 50%;
		animation: spin 360s infinite linear;
	}

	.content :global(span) {
		position: absolute;
	}

	@keyframes spin {
		from {
			transform: translate(-50%, -50%) rotate(0deg);
		}
		to {
			transform: translate(-50%, -50%) rotate(360deg);
		}
	}

	@media screen and (max-width: 1079px) {
		.content {
			flex-direction: column;
		}

		.skill-list {
			width: 100%;
			height: auto;
			padding-top: 20px;
		}

		.circle-words {
			width: 100%;
		}
	}

	@media screen and (max-width: 439px) {
		.skill-box {
			height: auto;
		}
	}
</style>
