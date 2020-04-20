<script>
	import { pets } from '../stores.js'
	import Pet from './Pet.svelte'

	function handleRemovePet(e) {
		pets.update(pets => pets.filter(p => p.name !== e.detail))
	}

	function handleClearAll() {
		pets.set([])
	}
</script>

<div class="pets">
	{#each $pets as pet}
		<Pet {pet} on:removePet={handleRemovePet} />
	{:else}
		<p>Empty waiting list...</p>
	{/each}
	{#if $pets.length >= 1}
		<button on:click={handleClearAll}>Clear All</button>
	{/if}
</div>
