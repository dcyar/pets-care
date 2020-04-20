<script>
	import { createEventDispatcher } from 'svelte'

	export let pet

	const dispatch = createEventDispatcher()

	function handleRemove(name) {
		dispatch('removePet', name)
	}
</script>

<style>
	.pet {
		border: 1px solid #eee;
		text-align: left;
		padding: 5px 10px;
		margin-bottom: 10px;
		display: grid;
		grid-template-columns: 2fr 1fr;
	}
	.pet .description p {
		margin: 0;
	}
	.pet .actions {
		text-align: right;
		vertical-align: middle;
	}
	.pet .actions span {
		background-color: transparent;
		color: #eee;
		cursor: pointer;
		font-size: 16px;
	}
</style>

<div class="pet">
	<div class="description">
		<p>
			<strong>Name:</strong>
			{pet.name}
		</p>
		<p>
			<strong>Age:</strong>
			{pet.age} months
		</p>
	</div>
	<div class="actions">
		<span on:click={handleRemove(pet.name)}>X</span>
	</div>
</div>
