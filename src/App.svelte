<script>
	// VIDS 1-8
	// const name = "Jim";
	// const lastName = "<b>Lougheed</b>";
	// const hack = `<a href="#" onclick="alert('You have been hacked!')">Win a prize!</a>`;
	// const id = "heading";
	// const disabled = false;
	// const status = "success";
	// const isPromoted = true;
	// const promoted = true;

	// VIDS 9-
	const num = 5;
</script>

<main>
	<!-- VIDS 1-8 -->
	<!-- <h1>Hello, {name}!</h1>
	<div>{@html lastName}</div>
	<div>{@html hack}</div>
	<h2 class="underline" {id}>This is a heading</h2>
	<h2 class={status}>Status</h2> -->

	<!-- <h2 class={isPromoted ? "promoted" : ""}>Movie Title</h2> -->
	<!-- <h2 class:promoted={isPromoted}>Movie Title</h2> -->
	<!-- <h2 class:promoted>Movie Title</h2>

	<button {disabled}>Bind</button> -->

	<!-- VIDS 9- -->
	{#if num === 0}
	<h2>The number is 0</h2>
	{:else if num < 0}
	<h2>The number is negative</h2>
	{:else if num > 0}
	<h2>The number is positive</h2>
	{:else}
	<h2>The number is not a number</h2>
	{/if}
</main>

<style>
	/* VIDS 1-8 */
	/* .underline {
		text-decoration: underline;
	}
	.danger {
		color: red;
	}
	.success {
		color: olivedrab;
	}
	.promoted {
		font-style: italic;
	} */
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>