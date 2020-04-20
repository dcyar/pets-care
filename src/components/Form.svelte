<script>
	import { pets } from '../stores.js'

	let name = ''
	let age = ''

	function handleStorePet() {
		pets.update(p => [
			{
				name: name,
				age: age
			},
			...$pets
		])

		document.querySelector('.form').reset()
	}
</script>

<style type="text/css">
	.form-control {
		width: 100%;
		background-color: transparent;
		color: #eee;
	}

	button {
		width: 100%;
		background-color: transparent;
		color: #eee;
	}

	button:focus {
		background-color: #2b0b38;
	}
</style>

<div>
	<h3>Add Pet</h3>
	<form action="" class="form" on:submit|preventDefault={handleStorePet}>
		<input
			type="text"
			class="form-control"
			name="name"
			bind:value={name}
			placeholder="Enter pet name..." />
		<input
			type="number"
			class="form-control"
			name="age"
			bind:value={age}
			min="1"
			max="12"
			placeholder="Enter pet age..." />
		<button type="submit">Save Pet</button>
		<button type="reset">reset</button>
	</form>
</div>
