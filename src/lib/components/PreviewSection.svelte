<script lang="ts">
	// @ts-ignore
	const excerpts = [
		{
			number: 1,
			title: 'Buying a Deck',
			strapline: 'How to Choose Your Deck',
			// @ts-ignore
			text: `For the agnostic method we will be using a Tarot de Marseille. The deck should be a tarot deck They are usually easiest to get online. You can buy them on Amazon, or at the publisher's websites. This class will be using the CBD tarot in particular.For this course you will need a Tarot de Marseille deck. It should be a classic replica. It needs to be an actual tarot deck. What I mean is 78 cards comprised of 22 major arcana, 40 pip cards and 16 court cards. There are several decks for sale on Amazon or the publishers websites. Below are two recommendations:

`
		},
		{
			number: 2,
			title: 'Why Tarot de Marseille?',
			strapline: 'Tarot de Marseille Simplifies Leaning How to Read',
			// @ts-ignore
			text: `
When reading the cards there is quite a difference between using the Tarot de Marseille and the Rider Waite Smith deck. The RWS deck has scenic pip cards meaning there are people and scenes portrayed on each card. The TdM does not, each pip is simply the rank / number of suit symbols, for example the three of cups shows three cups. The TdM has decorative flourishes on the pips but no scenes.

Aside from that difference, The RWS is based on Western Hermeticism. The cards all carry significant mystical symbolism which colors the meaning of the cards. This makes some of the cards feel unapproachable to me. In this chapter I am going to compare some cards from the two decks to show how much the RWS is influenced by Hermeticism and pont out the difference in charm.`
		},
		{
			number: 3,
			title: 'The Agnostic Method',
			strapline: 'Practice Reading for Fun and Enrichment',
			// @ts-ignore
			text: `To become good at reading the cards you need practice, lots of practice. How do you get practice when you don't know how to read? How do you learn how to read without practice? Experience beats all when it comes to good readings. With experience comes confidence, which brings daring and openness. You are given the boldness to move forward in spite of fear.

I am proposing to make a practice of reading the cards. Each day you pick up the deck and shuffle it and do several readings. You handle the cards, a lot. There is more to it, and I will explain in detail in the coming pages, but the goal here is to make the deck a well used tool.

The Tarot de Marseille is ideal for this purpose because it is free of religious and occultic influences, which adds a lot of extra information you don't need for reading the cards. Information overload is a thing, and it slows down learning. It is also discouraging in my opinion.
    `
		},
		{
			number: 4,
			title: 'The Fool, Le Mat',
			strapline: 'The Fool Represents the Querant, and All of Us',
			text: 'The fool in the TdM is different than the fool in the RWS...'
		},
		{
			number: 5,
			title: 'Number 5',
			strapline: 'This is Numero Cinco',
			text: 'I am looking forward to Cinco de Mayo :)'
		}
	];

	let selectedExcerptNumber = $state(1);

	const selectExcerpt = (excerpt: {
		number: number;
		title?: string;
		strapline?: string;
		text?: string;
	}) => {
		selectedExcerptNumber = excerpt.number;
	};
	let selectedExcerpt = $derived(
		excerpts.find((excerpt) => excerpt.number === selectedExcerptNumber)
	);
</script>

<section class="chapter-preview default-margin">
	<h2 class="mb-l">What You're Getting</h2>
	<div class="chapter-container">
		<ul>
			{#each excerpts as excerpt}
				<li>
					<button
						class="chapter-title"
						aria-controls={`chapter-info-${excerpt.number}`}
						class:selected-chapter-title={selectedExcerptNumber === excerpt.number}
						aria-expanded={selectedExcerptNumber === excerpt.number}
						onclick={() => selectExcerpt(excerpt)}
					>
						<h4>Chapter {excerpt.number}: {excerpt.title}</h4>
					</button>
				</li>
			{/each}
		</ul>
		<div class="chapter-info">
			<h3 class="chapter-strapline italic mb-s">{selectedExcerpt?.strapline}</h3>
			<p>
				{selectedExcerpt?.text}
			</p>
		</div>
	</div>
</section>

<style>
	.chapter-preview {
		padding: 2rem 1rem;
		/* margin-left: 12vw; */
		/* margin-right: 20vw; */
		max-width: 1150px;
		height: 100vh;
	}
	.chapter-container {
		display: flex;
		justify-content: space-between;
	}
	.chapter-container ul {
		padding: 3rem 2rem;
		width: 40%;
	}
	.chapter-title {
		border-bottom: 1px solid grey;
		width: 100%;
		display: block;
		padding: 0.75rem;
		text-align: left;
		font-weight: 800;
	}
	.chapter-info {
		padding: 3rem 2rem;
		width: 55%;
	}
	.chapter-strapline {
		font-weight: normal;
	}
	.selected-chapter-title {
		background-color: black;
		color: white;
	}
</style>
