<script>
	import CoolButton from '../../components/CoolButton.svelte';
</script>

<svelte:head>
	<title>About</title>
	<meta name="description" content="About me" />
</svelte:head>

<div class="page">

	<div class="photo">
		<img src="/photo-opt.jpg" alt="Anton Khantelev" />
	</div>
	<div class="content">
		<div class="text">

			<div class="description">

				<p>
					I'm dedicated <b>middle+/senior</b> frontend developer with <b>more than 3 years</b> of commercial experience,
					contributing to innovative web applications and user interfaces.
				</p>
				<p>
					Proficient in front-end technologies, responsive design, and cross-browser compatibility.
					Strong collaborator with a passion for crafting seamless user experiences.
				</p>
				<p>
					Adept at translating design mockups and wireframes into responsive, interactive web
					applications.
				</p>
				<p>
					I have extensive knowledge in a client-server communication and in a security of web
					applications.
				</p>
				<p>
					I have strong experience in developing complex web applications and services, such as system
					for managing business processes and electronic document management.
				</p>

			</div>
			<div class="photo-space">

			</div>

			<div class="additional-info">
				<div>
					<h3>Education</h3>
					<p>St. Petersburg State Electrotechnical University "LETI" (2010 > 2014)</p>
					<p>Crisis management</p>
				</div>
				<div>
					<h3>Languages</h3>
					<ul>
						<li>
							English – B2 
						</li>
						<li>
							Russian - Native
						</li>	
					</ul>
				</div>
			</div>

	</div>
		
	</div>

	<div class="download-button-wrapper">
		<CoolButton />
	</div>

</div>

<style>
	.page {
		padding-top: var(--header-height);
		font-family: var(--font-mono);
		height: calc(100vh - var(--header-height));
		background: linear-gradient(
			-5deg,
			rgba(8, 10, 10) 33%,
			rgba(27, 34, 40)  34% 40%,
			rgba(28, 35, 41) 46%,
			rgba(32, 40, 47) 56%,
			rgba(35, 44, 51) 66%,
			rgba(33, 42, 49) 86%
		);
		background-attachment: fixed;
		position: relative;
	}

	.download-button-wrapper {
		display: flex;
		align-items: center;
		justify-content: center;
		position: absolute;
		bottom: 30px;
		left: 50%;
		transform: translateX(-50%);
	}

	.content {
		color: var(--color-text);
		position: relative;
		z-index: 1;
		width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		top: 15%;
	}

	.text {
		display: flex;
	}

	.text p, h3 {
		padding: 0 10px;
	}

	.description {
		width: 40%;
	}

	.photo-space {
		width: 20%;
	}

	.additional-info {
		display: flex;
		flex-direction: column;
		width: 40%;
	}

	.photo {
		width: 40%;
		display: flex;
		justify-content: center;
	}

	.photo img {
		height: calc(100vh - var(--header-height));
		opacity: 0.4;
		position: fixed;
		left: 50%;
		transform: translateX(-50%);
		top: var(--header-height);
	}

	.description {
		width: 40%;
	}

	.description p {
		font-family: var(--font-mono);
	}

	@media screen and (max-width: 1248px) {
		.download-button-wrapper {
			position: relative;
			bottom: 20px;
			left: 0;
			transform: none;
			margin-top: 50px;
		}

		.page {
			height: auto;
		}
	}


	@media screen and (max-width: 900px) {

	}

	@media screen and (max-width: 540px) {
		.text {
			flex-direction: column;
			width: 320px;
			align-items: center;
		}
		.description {
			width: 100%;
		}

		.additional-info {
			width: 100%;
		}

	}

	@media screen and (max-width: 360px) {
		.text {
			width: max(320px, 100%);
		}

		.page {
			width: max(320px, 100%);
		}

		.photo img {
			width: max(320px, 100%);
		}

	}
</style>
