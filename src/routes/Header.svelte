<script>
	import { page } from '$app/stores';

</script>

<header>
	<nav>
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : false}>
				<a href="/">Home</a>
			</li>
			<li aria-current={$page.url.pathname === '/aboutme' ? 'page' : false}>
				<a href="/aboutme">about me</a>
			</li>
			<li aria-current={$page.url.pathname === '/skills' ? 'page' : false}>
				<a href="/skills">skills</a>
			</li>
			<li aria-current={$page.url.pathname === '/experience' ? 'page' : false}>
				<a href="/experience">experience</a>
			</li>
			<li aria-current={$page.url.pathname === '/contacts' ? 'page' : false}>
				<a href="/contacts">contacts</a>
			</li>
		</ul>
	</nav>
	
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		position: absolute;
		top: 0;
		height: var(--header-height);
		width: 100%;
		z-index: 2;
	}

	[aria-current="page"] a {
		color: var(--color-theme-1);
	}

	nav {
		display: flex;
		justify-content: center;
		position: absolute;
		top: 0;
		left: 50%;
		transform: translateX(-50%);
		color: black;
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	header nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
		white-space: nowrap;
	}

	header nav li a:hover {
		color: var(--color-theme-1);
	}

	@media screen and (max-width: 430px) {
		header nav li a {
			font-size: 0.7rem;
			font-weight: normal;
		}
	}

	
	@media screen and (max-width: 380px) {
		header nav li a {
			font-size: 0.6rem;
			font-weight: normal;
		}
	}

	@media screen and (max-width: 340px) {
		header nav li a {
			font-size: 0.5rem;
			font-weight: normal;
		}
	}
</style>
