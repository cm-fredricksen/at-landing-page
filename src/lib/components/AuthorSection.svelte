<script>
	import authorPic from '$assets/cbd-tarot-images/a22.jpg';
</script>

<section class="author-section">
	<h2 class="mb-m mt-s">About the author</h2>
	<div class="author-container">
		<div class="author-text">
			<p class="mb-xs">
				Chris Fredricksen has been reading tarot for 30 years, and she has learned and used numerous
				systems including tarot, playing cards, oracle cards, various magicks, numerology, and more.
				She has also actively practiced journaling, meditation, tai chi, and taoism. She has studied
				several religious texts, and loves reading classic books, poetry, and inspired writings. All
				of this study and practice has led her to develop her own way of reading the tarot.
			</p>
			<p class="mb-xs">
				Chris takes a practical, down to earth approach to reading the cards. She has removed the
				spiritual and psychological connotations often associated with reading tarot. Instead her
				focus is on engaging the creative mind for real life problem solving(and fun).
			</p>
			<p class="mb-xs">She currently lives in Minnesota with her family.</p>
		</div>
		<img src={authorPic} alt="Author Chris Fredricksen" />
	</div>
</section>

<style>
	.author-section {
		padding: 3rem 2rem;
		height: 100vh;
		max-width: 100%;
		background-color: lavender;
	}
	.author-container {
		display: flex;
		justify-content: space-between;
	}

	.author-text {
		padding: 0 1rem;
		width: 55%;
	}
	img {
		padding: 0 1rem;
	}
</style>
