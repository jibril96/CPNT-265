<script>
	let title = 'CarZ';
</script>

<!DOCTYPE html />
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta http-equiv="X-UA-Compatible" content="IE=edge" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<link rel="stylesheet" href="styles.css" />
	</head>
	<body>
		<div class="wrapper">
			<section class="top-container">
				<header class="showcase">
					<h1>{title}</h1>
					<p>
						Welcome to CarZ where you will find your favorite sport cars. Pick your desired color
						and speed away!
					</p>
					<a href="#" class="btn">Pick YourZ</a>
				</header>
				<div class="top-box top-box-a">
					<h4>USED</h4>
					<p class="price">$99/mo</p>
					<a href="#" class="btn">Rent</a>
				</div>
				<div class="top-box top-box-b">
					<h4>NEW</h4>
					<p class="price">$180/mo</p>
					<a href="#" class="btn">Rent</a>
				</div>
			</section>
			<section class="boxes">
				<div class="box">
					<h3>Our connections</h3>
					<p>
						Italy, United States, England, United Arab Emirates, Japan, France, Germany, China,
						Poland, and many more.
					</p>
				</div>
				<div class="box">
					<h3>Locations</h3>
					<p>Calgary, Toronto, vancouver, montreal, and Mississauga.</p>
				</div>
				<div class="box">
					<h3>We offer</h3>
					<p>
						We got all types of, new or used, sport cars from all over the globe. We got some
						classics too!
					</p>
				</div>
				<div class="box">
					<h3>Buy or Rent</h3>
					<p>
						pay month-to-month for any of your favorite color for low as $99/mo, or $180/ for new to
						rent or to buy. Your Demon is waiting for you, come get it!
					</p>
				</div>
			</section>
			<section class="info">
				<img src="/images/insidecar.jpeg" alt="insidecar" />
				<div>
					<h2>The choice is yours</h2>
					<p>
						we offer top quality fast, sport cars. Our company has connection throughout the world,
						and because of that we got foreign on foreign. We have your color in mind! We leave it
						up to you to choose what you want.
					</p>
					<a href="#" class="btn">check it out</a>
				</div>
			</section>
			<section class="speed">
				<img src="/images/blackcar.jpeg" alt="" />
				<img src="/images/greycar.jpeg" alt="" />
				<img src="/images/redcar.jpeg" alt="" />
				<img src="/images/bluecar.jpeg" alt="" />
				<img src="/images/whitecar.jpeg" alt="" />
				<img src="/images/slivercar.jpeg" alt="" />
				<img src="/images/classiccar.jpeg" alt="" />
				<img src="/images/greencar.jpeg" alt="" />
				<img src="/images/yellowcar.jpeg" alt="" />
			</section>
		</div>
	</body>
</html>

<style>
	html {
		box-sizing: border-box;
		font-family: Arial, Helvetica, sans-serif;
		color: rgb(0, 0, 0);
	}

	body {
		background: #008000;
		margin: 30px 50px;
		line-height: 1.4;
	}

	.btn {
		background: rgb(153, 57, 57);
		color: rgba(0, 0, 0, 0.849);
		padding: 0.6rem 1.3rem;
		text-decoration: none;
		border: 0;
	}

	.btn:hover {
		color: blueviolet;
		background: pink;
	}

	img {
		max-width: 100%;
	}

	.wrapper {
		display: grid;
		grid-gap: 20px;
	}

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
		color: lightgrey;
		text-transform: uppercase;
		font-size: 1.1rem;
	}

	.main-nav a:hover {
		background: blue;
		color: red;
	}

	.top-container {
		display: grid;
		grid-gap: 20px;
		grid-template-areas:
			'showcase showcase top-box-a'
			'showcase showcase top-box-b';
	}

	.showcase {
		grid-area: showcase;
		min-height: 400px;
		background: url(/images/fastcar.jpeg);
		background-size: cover;
		background-position: center;
		padding: 3rem;
		display: flex;
		flex-direction: column;
		align-items: start;
		justify-content: center;
	}

	.showcase h1 {
		font-size: 4rem;
		margin-bottom: 0;
		color: red;
	}

	.showcase p {
		font-size: 1.3rem;
		margin-top: 0;
		color: yellow;
	}

	.top-box {
		background: #006400;
		display: grid;
		align-items: center;
		justify-items: center;
		padding: 1.5rem;
	}

	.top-box:hover {
		color: blue;
	}

	h4 {
		color: blue;
	}

	.top-box .price {
		font-size: 2.5rem;
	}

	.top-box-a {
		grid-area: top-box-a;
		color: yellow;
	}
	.top-box-b {
		grid-area: top-box-b;
		color: yellow;
	}

	.boxes {
		display: grid;
		grid-gap: 20px;
		grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
	}
	.box {
		background: rgb(0, 0, 0);
		text-align: center;
		padding: 1.5rem 2rem;
		color: rgb(255, 255, 255);
	}

	.info {
		display: grid;
		grid-gap: 30px;
		grid-template-columns: repeat(2, 1fr);
		padding: 3rem;
	}

	.speed {
		display: grid;
		grid-gap: 20px;
		grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
	}

	.speed img {
		width: 100;
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
