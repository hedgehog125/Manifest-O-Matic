<script>
	export let categories;
	export let onSubmit;

	let output = {};

	const onSubmitInternal = e => {
		onSubmit(output);
	};
</script>

<main>
	<form on:submit|preventDefault={onSubmitInternal}>
		{#each categories as category}
			<h2>
				{category.display}
			</h2>

			{#each category.properties as property}
				<label for={property.id}>
					{property.label}
				</label>
				<input bind:value={output[property.id]} type={property.type} name={property.id} placeholder={property.placeholder?? ""}>
			{/each}
		{/each}
	</form>
</main>