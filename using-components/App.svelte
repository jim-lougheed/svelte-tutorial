<script>
	// VIDS 17-18
    // import Greet from "./components/Greet.svelte";
	// const userName = "Jim";
	// const job = "developer";
	// const obj = {
	// 	name: "Barry",
	// 	heroName: "The Flash",
	// }

	// VID 19
	// import ComponentC from "./components/ComponentC.svelte";
	// import { setContext } from "svelte";

	// const userName = "Jim";
	// setContext('username-context', userName);

	// VID 20
	// import Popup from "./components/Popup.svelte";

	// let showPopup = false;

	// function closePopup(event) {
	// 	showPopup = false;
	// 	console.log(event.detail);
	// }

	// import Outer from "./components/Outer.svelte";

	// function handleGreet(event) {
	// 	alert(event.detail);
	// }

	// VID 21
	// import Button from "./components/Button.svelte";

	// VID 22
	// import Card from "./components/Card.svelte";

	// VID 24
	// import NameList from "./components/NameList.svelte";

	// VID 25
	import ChildStyles from "./components/ChildStyles.svelte";
</script>

<main>
	<!-- VIDS 17-18 -->
	<!-- <Greet name="Bruce" heroName="Batman"></Greet>
	<Greet name="Clark" heroName="Superman"></Greet>
	<Greet name="Diana" heroName="Wonder Woman"></Greet>
	<Greet name={userName} heroName={job}></Greet>
	<Greet {...obj}></Greet> -->

	<!-- VID 19 -->
	<!-- <h2>App Component Username - {userName}</h2>
	<ComponentC></ComponentC> -->

	<!-- VID 20 -->
	<!-- <button on:click={() => showPopup = true}>Show Popup</button>
	{#if showPopup} -->
		<!-- <Popup on:close={() => showPopup = false}></Popup> -->
		<!-- <Popup on:close={closePopup}></Popup>
	{/if} -->

	<!-- VID 21 -->
	<!-- <Outer on:greet={handleGreet}></Outer>
	<Button on:click={() => alert('Clicked')}></Button> -->
	
	<!-- VID 22 -->
	<!-- <Card>Card content 1</Card>
	<Card><h2>Card content 2</h2></Card>
	<Card><img src="http://picsum.photos/200" alt="sample"/></Card>
	<Card></Card> -->

	<!-- VID 23 -->
	<!-- <Card>
		<div slot="header">
			<h3>Header</h3>
		</div>
		<div slot="content">
			<img src="http://picsum.photos/200" alt="sample"/>
		</div>
		<div slot="footer">
			<button>View Details</button>
		</div>
	</Card> -->

	<!-- VID 24 -->
	<!-- <NameList>
		<h3 slot="hero" let:firstName let:lastName>{firstName} {lastName}</h3>
	</NameList>
	<NameList>
		<h3 slot="hero" let:firstName let:lastName>{lastName}, {firstName}</h3>
	</NameList>
	<NameList>
		<h3 slot="hero" let:firstName>{firstName}</h3>
	</NameList> -->

	<!-- VID 25 -->
	<h4>App component text</h4>
	<h3>App component global style</h3>
	<ChildStyles></ChildStyles>
</main>

<style>
	:global(h3) {
		color: blue;
	}
	h4 {
		color: orange;
	}
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