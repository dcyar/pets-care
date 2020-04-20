<script>
	import { pets } from '../stores.js'

	let name = ''
	let age = 1

	function handleStorePet() {
		if (name != '' && age > 0) {
			pets.update(() => [
				{
					name: name,
					age: age
				},
				...$pets
			])
			name = ''
			age = 1
		}
	}
</script>

<style type="text/css">
	.form-control {
		width: 100%;
		background-color: transparent;
		color: #eee;
	}
</style>

<div>
	<h3>Pet Data</h3>
	<form action="" class="form" on:submit|preventDefault={handleStorePet}>
		<input
			type="text"
			class="form-control"
			name="name"
			minlength="3"
			bind:value={name}
			required
			placeholder="Enter pet name..." />
		<input
			type="number"
			class="form-control"
			name="age"
			bind:value={age}
			min="1"
			max="24"
			placeholder="Enter pet age..." />
		<button type="submit">Add Pet</button>
	</form>
</div>
