<script>
	import CharityList from "../components/CharityList.svelte";

	let title = "Charity";

	let charities = ["Charity 1", "Charity 2", "Charity 3"];
</script>

<div>
	<h1>{title}</h1>
	<!-- mengirimkan data charities -->
	<!-- <CharityList charities = {charities} /> -->
	<CharityList {charities} />
</div>

<style>
	h1 {
		font-size: 3em;
		color: #e2071c;
	}
</style>
