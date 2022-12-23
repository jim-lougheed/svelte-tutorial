<script>
	// VIDS 17-18
    // import Greet from "./components/Greet.svelte";
	// const userName = "Jim";
	// const job = "developer";
	// const obj = {
	// 	name: "Barry",
	// 	heroName: "The Flash",
	// }

	// VIDS 19-
	import ComponentC from "./components/ComponentC.svelte";
	import { setContext } from "svelte";

	const userName = "Jim";
	setContext('username-context', userName);

	import Popup from "./components/Popup.svelte";

	let showPopup = false;

	function closePopup(event) {
		showPopup = false;
		console.log(event.detail);
	}

	import Outer from "./components/Outer.svelte";

	function handleGreet(event) {
		alert(event.detail);
	}

	import Button from "./components/Button.svelte";
</script>

<main>
	<!-- VIDS 17-18 -->
	<!-- <Greet name="Bruce" heroName="Batman"></Greet>
	<Greet name="Clark" heroName="Superman"></Greet>
	<Greet name="Diana" heroName="Wonder Woman"></Greet>
	<Greet name={userName} heroName={job}></Greet>
	<Greet {...obj}></Greet> -->

	<!-- VIDS 19- -->
	<h2>App Component Username - {userName}</h2>
	<ComponentC></ComponentC>

	<button on:click={() => showPopup = true}>Show Popup</button>
	{#if showPopup}
		<!-- <Popup on:close={() => showPopup = false}></Popup> -->
		<Popup on:close={closePopup}></Popup>
	{/if}

	<Outer on:greet={handleGreet}></Outer>
	<Button on:click={() => alert('Clicked')}></Button>
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