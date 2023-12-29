<script>
</script>

<svelte:head>
	<title>Expirience</title>
	<meta name="description" content="Expirience" />

	<style>
		header nav a {
			color: rgba(255, 255, 255, 0.7);
		}
	</style>
</svelte:head>

<div class="page">
	<div class="scrollbar" />
	<div class="container">
		<div class="job">
			<h2 class="job-title">// Web Solutions Developer</h2>
			<h3 class="company">
				DocsVision <span class="dates">/ 2021-2023 </span><span> / (2 years 5 months)</span>
			</h3>

			<div class="description">
				<p>
					\ Development of low-code platform, system for managing business processes and electronic
					document management
				</p>
				<p>
					\ Conducted a security audit of the application and eliminated vulnerabilities which could
					potentially lead to losses in millions and reputational damage
				</p>
				<p>
					\ Significantly improved the key components of the app to handle the display and
					manipulation of massive amounts of data, and dedicated myself to making this as efficient
					and user-friendly as possible
				</p>
				<p>
					\ Improved quality of existed architecture through refactoring and by implementing new
					strategies and best practices which made code base of entire app more clean, reliable and
					expandable and made opportunity to scale and deliver new features faster
				</p>
				<p>
					\ Conducted 8 meetups inside company and increased base level of skills and knowledges in
					a team
				</p>
				<p>
					\ Was salving unique, complex and urgent problems as third line of support for need of
					biggest companies of Russia and CIS
				</p>
			</div>
			<div class="separator" />
		</div>

		<div class="job">
			<h2 class="job-title">Web Developer</h2>
			<h3 class="company">
				BeeJee <span class="dates"> / 2020-2021 </span><span> / (7 months)</span>
			</h3>

			<div class="description">
				<p>\ Development of corporate CRM system</p>
				<p>
					\ Implementation of new features and enhancements, contributing to the overall improvement
					of user interfaces and user experiences
				</p>
				<p>
					\ My main achievement is getting skill of closely collaboration with cross-functional
					teams, including designers, product managers, and backend developers, to ensure seamless
					integration and delivery of features
				</p>
			</div>
			<div class="separator" />
		</div>

		<div class="job">
			<h2>Pet projects</h2>

			<div class="project-item">
				When I have free time, I like to use my skills to do something useful, so I made a few full
				stack applications you can check on my github account(akhant):
				<p>
					\ <a href="https://github.com/akhant/repemorizer">Repemorizer</a> - an application for learning
					languages using the spaced repetition method
				</p>
				<p>
					\ <a href="https://github.com/akhant/TrainingDiary">Training Diary</a> - application for training
					and statistics
				</p>
				<p>
					\ <a href="https://github.com/akhant/palabras">Palabras</a> - React Native app for learning
					Spanish
				</p>
				<p>
					\ <a href="https://github.com/akhant/website">Website</a> - This website which was created
					with Svelte and SvelteKit with server side rendering
				</p>
			</div>
		</div>
	</div>
</div>

<style>
	.page {
		background-color: #222;
		color: #ddd;
		font-size: 18px;
		line-height: 1.4;
		font-weight: 300;
		padding-top: var(--header-height);
		font-family: var(--font-mono);
		height: calc(100vh - var(--header-height));
		margin: 0;
		background: black;
		width: 100%;
		height: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
		padding-bottom: 40vh;
	}

	h2 {
		font-size: 21px;
		font-weight: bold;
	}

	h3 {
		font-size: 17px;
		font-weight: bold;
	}

	@property --scroll-y-position {
		syntax: '<percentage>';
		initial-value: -10%;
		inherits: false;
	}
	@property --reflection-y-position {
		syntax: '<percentage>';
		initial-value: -50%;
		inherits: false;
	}
	@property --scrollbar-color {
		syntax: '<color>';
		inherits: false;
		initial-value: transparent;
	}
	@property --opacity-1 {
		syntax: '<number>';
		inherits: false;
		initial-value: 0.1;
	}
	@property --opacity-2 {
		syntax: '<number>';
		inherits: false;
		initial-value: 0.1;
	}
	@property --opacity-3 {
		syntax: '<number>';
		inherits: false;
		initial-value: 0.1;
	}
	@property --opacity-4 {
		syntax: '<number>';
		inherits: false;
		initial-value: 0.1;
	}

	@property --text-offset-1 {
		syntax: '<number>';
		inherits: false;
		initial-value: 10;
	}
	@property --text-offset-2 {
		syntax: '<number>';
		inherits: false;
		initial-value: 10;
	}
	@property --text-offset-3 {
		syntax: '<number>';
		inherits: false;
		initial-value: 10;
	}
	@property --text-offset-4 {
		syntax: '<number>';
		inherits: false;
		initial-value: 10;
	}

	.scrollbar {
		width: 4px;
		height: 100%;
		background-color: var(--scrollbar-color);
		background-image: radial-gradient(
			circle at 0% var(--scroll-y-position),
			rgb(112, 153, 255) 0%,
			rgba(56, 106, 249, 0.79135) 10px,
			rgba(10, 76, 242, 0.53) 20px,
			rgba(255, 255, 255, 0) 40px,
			rgba(49, 49, 49, 0) 100%
		);
		animation: on-scrolling both linear;
		animation-timeline: scroll();
		animation-range: 10vh;
	}

	.container {
		width: max(320px, 40%);
		height: 100%;
		background: linear-gradient(
			132deg,
			rgba(255, 255, 255, 0.09) 0%,
			rgba(238, 238, 238, 0.03) 20%,
			rgba(202, 202, 202, 0.04) 70%,
			rgba(171, 171, 171, 0.02) 100%
		);
		border: solid rgba(255, 255, 255, 0.06) 1px;
		margin-left: 15px;
		position: relative;
		margin-top: 100px;
		z-index: 2;
	}
	.container::before,
	.container::after {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		display: block;
		width: 100%;
		height: 100%;
		background: linear-gradient(
			180deg,
			rgba(10, 76, 242, 0) 0%,
			rgba(10, 76, 242, 0.75203) 38.288288288288285%,
			rgb(77, 127, 255) 50.9132179054054%,
			rgba(10, 76, 242, 0.75248) 63.06306306306306%,
			rgba(10, 76, 242, 0) 100%
		);
		background-repeat: no-repeat;
		background-position-y: var(--reflection-y-position);
		animation: on-scrolling both linear;
		animation-timeline: scroll();
		animation-range: 10vh;
		z-index: 1;
	}
	.container::before {
		background-size: 1px 150px;
		filter: blur(1px);
	}
	.container::after {
		background-size: 10px 150px;
		filter: blur(10px);
	}

	.separator {
		height: 2px;
		width: 80%;
		background-color: rgba(255, 255, 255, var(--opacity-1));
		margin: 45px auto 5px;
	}

	.job {
		background-image: linear-gradient(
			270deg,
			rgba(255, 255, 255, 0.4) 0%,
			rgba(255, 255, 255, 0.9) 90%,
			rgb(191, 209, 255) 100%
		);
		background-clip: text;
		-webkit-background-clip: text;
		color: transparent;
		padding: 20px;
		line-height: 1.5em;
		--opacity-1: 0.1;
		--opacity-2: 0.1;
		--opacity-3: 0.1;
		--opacity-4: 0.1;
		--text-offset-1: 10;
		--text-offset-2: 10;
		--text-offset-3: 10;
		animation: on-scrolling both linear;
		animation-timeline: scroll();
		animation-range: 10vh;
		z-index: 3;
		position: relative;
	}

	.container::after {
		z-index: 2;
	}

	.job:nth-child(1) {
		opacity: var(--opacity-1);
		transform: translateY(calc(var(--text-offset-1) * 1px));
	}
	.job:nth-child(2) {
		opacity: var(--opacity-2);
		transform: translateY(calc(var(--text-offset-2) * 1px));
	}
	.job:nth-child(3) {
		opacity: var(--opacity-3);
		transform: translateY(calc(var(--text-offset-3) * 1px));
	}
	.job:nth-child(4) {
		opacity: var(--opacity-4);
		transform: translateY(calc(var(--text-offset-4) * 1px));
	}

	@keyframes on-scrolling {
		0% {
			--scroll-y-position: 10%;
			--reflection-y-position: 22%;
			--opacity-1: 1;
			--opacity-2: 0.1;
			--opacity-3: 0.1;
			--opacity-4: 0.1;

			--text-offset-1: 0;
			--text-offset-2: 10;
			--text-offset-3: 10;
			--text-offset-4: 10;
		}
		1% {
			--scrollbar-color: rgba(255, 255, 255, 0.1);
		}
		5% {
			--opacity-1: 1;
			--opacity-2: 0.1;
			--opacity-3: 0.1;
			--opacity-4: 0.1;

			--text-offset-1: 0;
			--text-offset-2: 10;
			--text-offset-3: 10;
			--text-offset-4: 10;
		}
		50% {
			--scroll-y-position: 50%;
			--reflection-y-position: 50%;
			--opacity-1: 0.1;
			--opacity-2: 1;
			--opacity-3: 0.1;
			--opacity-4: 0.1;

			--text-offset-1: 10;
			--text-offset-2: 0;
			--text-offset-3: 10;
			--text-offset-4: 10;
		}
		80% {
			--opacity-1: 0.1;
			--opacity-2: 0.1;
			--opacity-3: 1;
			--opacity-4: 0.1;

			--text-offset-1: 10;
			--text-offset-2: 10;
			--text-offset-3: 0;
			--text-offset-4: 10;
		}
		95% {
			--opacity-1: 0.1;
			--opacity-2: 0.1;
			--opacity-3: 0.1;
			--opacity-4: 1;

			--text-offset-1: 10;
			--text-offset-2: 10;
			--text-offset-3: 10;
			--text-offset-4: 0;
		}
		100% {
			--text-offset-1: 10;
			--text-offset-2: 10;
			--text-offset-3: 10;
			--text-offset-4: 10;
			--opacity-1: 0.1;
			--opacity-2: 0.1;
			--opacity-3: 0.1;
			--opacity-4: 0.1;
			--scroll-y-position: 105%;
			--reflection-y-position: 115%;
			--scrollbar-color: rgba(255, 255, 255, 0.1);
		}
	}
</style>
