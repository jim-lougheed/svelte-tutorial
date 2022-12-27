<script>
	// VID 27
    //import PostList from "./components/PostList.svelte";

	// VID 28
	import AutoFocus from "./components/AutoFocus.svelte";
</script>

<main>
	<!-- VID 27 -->
	<!-- <PostList></PostList> -->

	<!-- VID 28 -->
	<AutoFocus></AutoFocus>
</main>

<style>
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