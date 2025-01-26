<script>
	import leMat from '$assets/cbd-tarot-images/a22.jpg';
	import threeCoins from '$assets/cbd-tarot-images/d03.jpg';
	import queenBatons from '$assets/cbd-tarot-images/b13.jpg';
	import aceCups from '$assets/cbd-tarot-images/c01.jpg';
	import { Button } from '$components';
</script>

<section class="hero">
	<div class="hero-showcase text-center bold">
		<h1 class="text-color">UNDERSTAND</h1>
		<h1 class="text-color mb-s">TAROT CARDS</h1>
		<p class="italic semi-bold mb-m text-color">
			A simple way to learn using the TAROT de MARSEILLE. Beginning in the 1400's the tarot was a
			popular card game in Europe, and the images represent the times they were made in.
		</p>
		<img class="card-img" title="The Fool &copy;CBD Tarot" src={leMat} alt="" />
		<img class="card-img" title="The Ace of Cups &copy;CBD Tarot" src={aceCups} alt="" />
		<img class="card-img" title="The Queen of Batons &copy;CBD Tarot" src={queenBatons} alt="" />
		<img class="card-img" title="The Three of Coins &copy;CBD Tarot" src={threeCoins} alt="" />
	</div>
	<div class="hero-text white text-center">
		<h1>LEARN HOW TO</h1>
		<h1>READ TAROT</h1>
		<h1 class="mb-s">THE EASY WAY</h1>
		<p class="light-grey mb-l">
			No occultic meanings, no psychological terminology, no woo, no bullshit! With <span
				class="tam">The Agnostic Method</span
			> the number of meanings you need to learn is cut in half! We start with simple building blocks
			and actual hands-on practice to bring the tarot right down to earth.
		</p>
		<Button>Purchase the E-book for $10</Button>
	</div>
</section>

<style>
	section.hero {
		display: flex;
		height: 100vh;
		overflow-y: hidden;
	}
	.hero-showcase {
		width: 50%;
		padding: 3rem 2rem;
		/* background-color: lightseagreen; */
		background-color: lavender;
	}
	.hero-text {
		background-color: black;
		padding: 3rem 2rem;
		width: 50%;
	}
	.card-img {
		border: 1px solid black;
		border-radius: 0.5rem;
		margin: 0 0.5rem;
		height: 40%;
	}
	.tam {
		font-style: oblique;
		color: lavender;
	}
	.text-color {
		color: black;
	}
</style>
