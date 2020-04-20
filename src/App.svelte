<script>
	import Form from './components/Form.svelte'
	import WaitingList from './components/WaitingList.svelte'
</script>

<style>
	.container {
		text-align: center;
		padding: 1em;
		width: 95vw;
	}

	.wrap {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		column-gap: 10px;
		margin-top: 40px;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
		margin: 0;
	}

	@media (min-width: 640px) {
	}
</style>

<div class="container">
	<h1>Pets!</h1>
	<p>Atention of the pets</p>
	<div class="wrap">
		<Form />
		<WaitingList />
	</div>
</div>
