<script lang="ts">
	import ChevronDown from '$assets/icons/chevron-down.svg';
	let {
		faq,
		isExpanded,
		...props
	}: { faq: { question: string; answer: string }; isExpanded: boolean } = $props();
</script>

<button class="container" class:container-expanded={isExpanded} {...props}>
	<div class="question-and-answer">
		<p class="question mb-s">{faq.question}</p>
		<p class="answer">
			{faq.answer}
		</p>
	</div>
	<img src={ChevronDown} alt="" />
</button>

<style>
	.container {
		display: flex;
		justify-content: space-between;
		align-items: flex-start;
		padding: 0.8rem;
		border-bottom: 2px solid lavender;
		text-align: left;
	}
	.question-and-answer {
		padding-right: 150px;
		flex-grow: 1;
	}
	.answer {
		opacity: 0;
		max-height: 0;
		overflow: hidden;
		transition: all 0.3s ease-out;
	}
	button img {
		width: 24px;
		height: 24px;
		transition: transform 0.3s linear;
	}
	.question {
		font-weight: 600;
	}
	.container-expanded img {
		transform: rotate(180deg);
	}

	.container-expanded .answer {
		max-height: unset;
		opacity: 1;
	}
</style>
