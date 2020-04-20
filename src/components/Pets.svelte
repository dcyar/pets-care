<script>
	import { pets } from '../stores.js'
	import Pet from './Pet.svelte'

	let allpets = []
</script>

<div class="pets">
	{#each $pets as pet}
		<Pet {pet} />
	{:else}
		<p>Empty waiting list...</p>
	{/each}
</div>
