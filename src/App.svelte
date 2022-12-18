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

	// VIDS 9-11
	// const num = 5;
	// const names = ["Bruce", "Clark", "Diana"];
	// const fullNames = [{firstName: "Bruce", lastName: "Wayne"}, {firstName: "Clark", lastName: "Kent"}, {firstName: "Princess", lastName: "Diana"}];

	// VID 12
	// let count = 0;

	// function handleClick(event, increment) {
	// 	console.log(event, increment);
	// 	count += increment;
	// }

	// VIDS 13-14
	// const formValues = {
	// 	name: '',
	// 	profileSummary: '',
	// 	country: '',
	// 	jobLocation: [],
	// 	remoteWork: false,
	// 	skillSet: [],
	// 	yearsOfExperience: '',
	// };
	// function handleFormSubmit(event) {
	// 	console.log("Form values: ", formValues);
	// }

	// VIDS 15
	let firstName = "Bruce";
	let lastName = "Wayne";
	$:fullName = `${firstName} ${lastName}`;

	let items = [
		{
			id: 1,
			title: "TV",
			price: 100,
		},
		{
			id: 2,
			title: "Phone",
			price: 200,
		},
		{
			id: 3,
			title: "Computer",
			price: 300,
		},
	];
	$:total = items.reduce((total, curr) => (total = total + curr.price), 0);
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

	<!-- VIDS 9-11 -->
	<!-- <h1>Number: {num}</h1>
	{#if num === 0}
	<h2>The number is 0</h2>
	{:else if num < 0}
	<h2>The number is negative</h2>
	{:else if num > 0}
	<h2>The number is positive</h2>
	{:else}
	<h2>The number is not a number</h2>
	{/if}

	<h1>Names:</h1>
	{#each names as name, index}
	<h2>{index + 1}: {name}</h2>
	{/each}
	{#each fullNames as name, index (name.first)}
	<h2>{index + 1}: {name.firstName} {name.lastName}</h2>
	{/each} -->

	<!-- VID 12 -->
	<!-- <button on:click={() => count = count + 1}>Count: {count}</button>
	<button on:click={(event) => handleClick(event, 5)}>Count: {count}</button>
	<button on:click={(event) => handleClick(event, 10)}>Count: {count}</button> -->

	<!-- VIDS 13-14 -->
	<!-- <div>
		<pre>
			{JSON.stringify(formValues, null, 4)}
		</pre>
	</div>
	<form on:submit|preventDefault={handleFormSubmit}>
		<div>
			<label for="name">Name</label>
			<input type="text" id="name" bind:value={formValues.name}/>
		</div>
		<div>
			<label for="profile">Profile Summary</label>
			<textarea id="profile" bind:value={formValues.profileSummary} />
		</div>
		<div>
			<label for="country">Country</label>
			<select name="" id="country" bind:value={formValues.country}>
				<option value="canada">Canada</option>
				<option value="india">India</option>
				<option value="japan">Japan</option>
			</select>
		</div>
		<div>
			<label for="jobLocation">Job Location</label>
			<select name="" id="jobLocation" bind:value={formValues.jobLocation} multiple>
				<option value="canada">Canada</option>
				<option value="india">India</option>
				<option value="japan">Japan</option>
			</select>
		</div>
		<div>
			<input type="checkbox" id="remoteWork" bind:checked={formValues.remoteWork}/>
			<label for="remoteWork">Open to remote work?</label>
		</div>
		<div>
			<label>Skill set</label>
			<input type="checkbox" id="html" value="html" bind:group={formValues.skillSet} />
			<label for="html">HTML</label>
			<input type="checkbox" id="css" value="css" bind:group={formValues.skillSet} />
			<label for="css">CSS</label>
			<input type="checkbox" id="javascript" value="javascript" bind:group={formValues.skillSet} />
			<label for="javascript">JavaScript</label>
		</div>
		<div>
			<label>Years of experience</label>
			<input type="radio" id="0-2" value="0-2" bind:group={formValues.yearsOfExperience} />
			<label for="0-2">0-2</label>
			<input type="radio" id="3-5" value="3-5" bind:group={formValues.yearsOfExperience} />
			<label for="3-5">3-5</label>
			<input type="radio" id="6-10" value="6-10" bind:group={formValues.yearsOfExperience} />
			<label for="6-10">6-10</label>
			<input type="radio" id="10-15" value="10-15" bind:group={formValues.yearsOfExperience} />
			<label for="10-15">10-15</label>
		</div>
		<div>
			<button>Submit</button>
		</div>
	</form> -->

	<!-- VIDS 15 -->
	<button on:click={() => {
		firstName = "Clark";
		lastName = "Kent";
	}}>Change name</button>
	<h2>{firstName} {lastName}</h2>
	<h2>{fullName}</h2>

	<button on:click={() => (items = [...items, { id: 4, title: "Keyboard", price: 50 }])}>Add item</button>
	<h2>Total - {total}</h2>
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

	/* VIDS 13- */
	input + label {
		display: inline-flex;
	}
	main {
		/* text-align: center; */
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