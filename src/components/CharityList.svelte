<script>
	// export menangkap data charities
	// tanpa export charities hanya menjadi state local biasa
	// export let charities = ["default charity 1"];

	export let charities;
</script>

<div>
	<h2>Daftar Charity</h2>
	{#if charities !== undefined}
		<ul>
			{#each charities as charity}
				<li>{charity}</li>
			{/each}
		</ul>
	{:else}
		<h5>Data belum tersedia</h5>
	{/if}
</div>
