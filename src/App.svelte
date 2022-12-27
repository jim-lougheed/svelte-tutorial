<script>
	// VID 27
    //import PostList from "./components/PostList.svelte";

	// VID 28
	// import AutoFocus from "./components/AutoFocus.svelte";

	// VID 29
	import TabA from "./components/TabA.svelte";
	import TabB from "./components/TabB.svelte";
	import TabC from "./components/TabC.svelte";

	let activeTab = TabA;
</script>

<main>
	<!-- VID 27 -->
	<!-- <PostList></PostList> -->

	<!-- VID 28 -->
	<!-- <AutoFocus></AutoFocus> -->

	<!-- VID 29 -->
	<button on:click={() => activeTab = TabA}>TabA</button>
	<button on:click={() => activeTab = TabB}>TabB</button>
	<button on:click={() => activeTab = TabC}>TabC</button>

	<!-- {#if (activeTab === 'TabA')}
		<TabA></TabA>
	{:else if (activeTab === 'TabB')}
		<TabB></TabB>
	{:else if (activeTab === 'TabC')}
		<TabC></TabC>
	{/if} -->
	<svelte:component this={activeTab}></svelte:component>
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