<script>
	// @ts-nocheck

	// @ts-ignore
	import { FaqItem, Button } from '$components';

	const faqs = [
		{
			question: 'Why Agnostic Tarot?',
			answer:
				'Agnostic tarot focuses on learning to read the cards through practice, leaving out the spiritual and psychological meanings. The approach is light, while you are learning. Once you feel comfortable with the cards, your understanding of the cards will grow.'
		},
		{
			question: 'Can I buy my own deck?',
			answer:
				"Yes, you can and should buy your own deck. Also you can just store the deck in the box it came in. You don't need to wrap it in silk, sleep with it under your pillow, or do any other rituals for this class. There is nothing wrong with any of those things - but it is not needed."
		},
		{
			question: 'Is tarot safe to use?',
			answer:
				'I would say it is safe with some caveats. If you are prone to anxiety, or feel fear about using the tarot, perhaps you should hold off. I take breaks from tarot when I feel very anxious, or limit the cards I can pull by removing any that make me feel anxious. Using tarot should be fun, and give encouragement.'
		},
		{
			question: 'Do I need psychic abilities to read tarot?',
			answer:
				'No, you do not need psychic abilities of any kind to read the cards. It is a skill you can learn with practice. The more you use the cards, the better you will get at reading them. '
		},
		{
			question: 'What do I need for this course?',
			answer:
				'For this class you need: a Tarot de Marseille deck, a notebook and a pen. There is a keyword keyword list included with the class to get you started. I will show you how to make your own lists too!'
		}
	];

	let questionCurrentlyExpanded = $state(-1);

	let onClick = (index) => {
		if (questionCurrentlyExpanded === index) {
			questionCurrentlyExpanded = -1;
		} else {
			questionCurrentlyExpanded = index;
		}
	};
</script>

<section class="faq-section section">
	<h2 class="mb-m mt-l">Frequently Asked Questions</h2>
	<div class="faq-container">
		{#each faqs as faq, index}
			<FaqItem
				{faq}
				isExpanded={index === questionCurrentlyExpanded}
				onclick={() => onClick(index)}
			/>
		{/each}
	</div>

	<div class="additional-info">
		<Button class="mt-l mb-s">Buy Now</Button>
		<p class="fs-s text-center">questions? Contact me:</p>
		<p class="text-center">
			<a href="mailto:cmfredricksen@gmail.com">cmfredricksen@gmail.com &clubs;</a>
		</p>
	</div>
</section>

<style>
	.faq-container {
		padding: 3rem 2rem;
	}
	.additional-info {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		opacity: 75%;
	}
	.additional-info a {
		text-decoration: underline;
		padding-bottom: 3rem;
	}
</style>
