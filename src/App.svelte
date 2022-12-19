<script>
    import Greet from "./components/Greet.svelte";
	const userName = "Jim";
	const job = "developer";
	const obj = {
		name: "Barry",
		heroName: "The Flash",
	}
</script>

<main>
	<Greet name="Bruce" heroName="Batman"></Greet>
	<Greet name="Clark" heroName="Superman"></Greet>
	<Greet name="Diana" heroName="Wonder Woman"></Greet>
	<Greet name={userName} heroName={job}></Greet>
	<Greet {...obj}></Greet>
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