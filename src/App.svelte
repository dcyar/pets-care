<script>
	import Form from './components/Form.svelte'
	import WaitingList from './components/WaitingList.svelte'
</script>

<style>
	.container {
		text-align: center;
		padding: 1em;
		width: 90vw;
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

	@media (max-width: 980px) {
		.wrap {
			grid-template-columns: 1fr;
		}
	}
</style>

<div class="container">
	<h1>Pets!</h1>
	<p>Pet care, wonderful pets and majestic pets</p>
	<div class="wrap">
		<Form />
		<WaitingList />
	</div>
</div>
