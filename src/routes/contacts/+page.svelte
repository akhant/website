<script>
	import github from '$lib/images/github.svg';
	import telegram from '$lib/images/telegram.png';
	import mail from '$lib/images/mail.png';
	import whatsapp from '$lib/images/whatsapp.png';
</script>

<svelte:head>
	<title>Contacts</title>
	<meta name="description" content="Contacts" />

	<style>
		header nav a {
			color: rgba(255, 255, 255, 0.7);
		}
	</style>

</svelte:head>

<div class="page">
	<div class="bg-shine dark">
		<div class="bg-shine_layer">
			<div class="jumbo" />
		</div>
		<h1>Contacts</h1>
		<div class="content">
			<div class="contact">
				<div class="contact-item">
					<div class="contact-item__icon">
						<img src={mail} alt="mail" />
					</div>
					<div class="contact-item__text">
						<a href="mailto:tangcossin@gmail.com" target="_blank">tangcossin@gmail.com</a>
					</div>
				</div>
				<div class="contact-item">
					<div class="contact-item__icon">
						<img src={telegram} alt="telegram" />
					</div>
					<div class="contact-item__text">
						<a href="https://t.me/antomic_reactor" target="_blank">
							<span>@antomic_reactor</span></a
						>
					</div>
				</div>
				<div class="contact-item">
					<div class="contact-item__icon">
						<img src={whatsapp} alt="whatsapp" />
					</div>
					<div class="contact-item__text">
						<a href="https://api.whatsapp.com/send?phone=79531560819" target="_blank"
							>+79531560819</a
						>
					</div>
				</div>
				<div class="contact-item item__github">
					<div class="contact-item__icon">
						<img src={github} alt="github" />
					</div>
					<div class="contact-item__text">
						<a href="https://github.com/akhant" target="_blank">akhant</a>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>

<style>

	.page {
		height: 100vh;
	}

	.contact {
		z-index: 2;
		background: rgba(255, 255, 255, 0.5);
		padding: 40px 80px;
		border-radius: 10px;
		width: 320px;
		box-sizing: border-box;
		display: flex;
		flex-direction: column;
		justify-content: left;
		align-items: baseline;
	}

	.contact-item {
		display: flex;
		z-index: 3;
		margin-top: 5px;
		align-items: center;
	}

	.contact-item__icon {
		margin-right: 10px;
		position: relative;
	}

	.contact-item__icon img {
		width: 25px;
	}

	.item__github img {
		width: 30px;
		position: relative;
		left: -3px;
	}

	.item__github .contact-item__text {
		position: relative;
		left: -5px;
	}

	.contact-item__text a {
		color: rgba(0,0,0,0.95);
		font-family: var(--fira-mono);
		transition: .3s;
	}

	.contact-item:hover .contact-item__text a {
		color: rgba(255,255,255, 0.9);

	}

	/* background animation */

	.bg-shine {
		position: relative;
		z-index: 0;
		display: flex;
		justify-content: center;
		flex-direction: column;
		transition-property: background;
		align-items: center;
		background-color: #000;
		height: 100vh;
	}

	.bg-shine_layer {
		position: absolute;
		overflow: hidden;
		top: 0px;
		left: 0px;
		right: 0px;
		bottom: 0px;
	}

	.jumbo {
		position: absolute;
		opacity: 0.5;
		top: 10px;
		left: 10px;
		right: 10px;
		bottom: 10px;
	}

	@keyframes jumbo {
		from {
			background-position: 50% 50%, 50% 50%;
		}
		to {
			background-position: 350% 50%, 350% 50%;
		}
	}

	.jumbo {
		--stripes: repeating-linear-gradient(
			100deg,
			#fff 0%,
			#fff 7%,
			transparent 10%,
			transparent 12%,
			#fff 16%
		);
		--stripesDark: repeating-linear-gradient(
			100deg,
			#000 0%,
			#000 7%,
			transparent 10%,
			transparent 12%,
			#000 16%
		);
		--rainbow: repeating-linear-gradient(
			100deg,
			#60a5fa 10%,
			#e879f9 15%,
			#60a5fa 20%,
			#5eead4 25%,
			#60a5fa 30%
		);
		background-image: var(--stripes), var(--rainbow);
		background-size: 300%, 200%;
		background-position: 50% 50%, 50% 50%;

		filter: blur(10px) invert(100%);

		mask-image: radial-gradient(ellipse at 100% 0%, black 40%, transparent 70%);

		pointer-events: none;
	}

	.jumbo::after {
		content: '';
		position: absolute;
		inset: 0;
		background-image: var(--stripes), var(--rainbow);
		background-size: 200%, 100%;
		animation: jumbo 60s linear infinite;
		background-attachment: fixed;
		mix-blend-mode: difference;
	}

	.dark .jumbo {
		background-image: var(--stripesDark), var(--rainbow);
		filter: blur(10px) opacity(50%) saturate(200%);
	}
	.dark .jumbo::after {
		background-image: var(--stripesDark), var(--rainbow);
	}

	/* bg-animation end */
</style>
