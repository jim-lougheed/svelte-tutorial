<script>
	import Decrement from "./components/Decrement.svelte";
import Display from "./components/Display.svelte";
    import Increment from "./components/Increment.svelte";
    import Reset from "./components/Reset.svelte";
    import Timer from "./components/Timer.svelte";
</script>

<main>

</main>
	<Display></Display>
	<Increment></Increment>
	<Decrement></Decrement>
	<Reset></Reset>

	<Timer></Timer>
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