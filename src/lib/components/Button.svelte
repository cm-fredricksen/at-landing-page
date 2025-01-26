<script>
	let { children, ...props } = $props();
</script>

<button {...props}>{@render children()}</button>

<style>
	button {
		color: white;
		background: black;
		border: 1px solid white;
		border-radius: 0.25rem;
		padding: 1rem 1.5rem;
		font-family: 'Montserrat', sans-serif;
		font-size: 1rem;
		font-weight: 600;
		text-transform: uppercase;
		transition: all 0.4s;

		&:hover {
			background-color: white;
			color: black;
		}
	}
</style>
