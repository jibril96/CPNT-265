<header>
    		<nav class="main-nav">
				<ul>
					<li>
						<a href="/">Home</a>
					</li>
					<li>
						<a href="/about">About</a>
					</li>
					<li>
						<a href="/services">services</a>
					</li>
					<li>
						<a href="/contact">contact</a>
					</li>
				</ul>
			</nav>
</header>

<main>
	<slot />
</main>

<footer>
    <p>Jibril &copy; 2022</p>
</footer>

<style>
.main-nav ul {
    display: grid;
    grid-gap: 20px;
    padding: 0;
    list-style: none;
    grid-template-columns: repeat(4, 1fr);
}

.main-nav a {
    background: black;
    display: block;
    text-decoration: none;
    padding: 0.8rem;
    text-align: center;
    color:lightgrey;
    text-transform: uppercase;
    font-size: 1.1rem;
}

.main-nav a:hover {
    background: blue;
    color: red;
}

	footer {
		margin-top: 1rem;
		background: black;
		color: white;
		text-align: center;
		padding: 0.5rem;
	}

	@media (max-width: 700px) {
		.top-container {
			grid-template-areas:
				'showcase showcase'
				'top-box-a top-box-b';
		}

		.showcase h1 {
			font-size: 2.5rem;
		}

		.main-nav ul {
			grid-template-columns: 1fr;
		}

		.info {
			grid-template-columns: 1fr;
		}
		.info .btn {
			display: block;
			text-align: center;
			margin: auto;
		}
	}

	@media (max-width: 500px) {
		.top-container {
			grid-template-areas:
				'showcase'
				'top-box-a'
				'top-box-b';
		}
	}
</style>
