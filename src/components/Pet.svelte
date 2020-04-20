<script>
	export let pet
</script>

<style>
	.pet {
		border: 1px solid #eee;
		text-align: left;
		padding: 5px 10px;
		margin-bottom: 10px;
	}
	.pet p {
		margin: 0;
	}
</style>

<div class="pet">
	<p>
		<strong>Name:</strong>
		{pet.name}
	</p>
	<p>
		<strong>Age:</strong>
		{pet.age} months
	</p>
</div>
