<script>
	import CenteredPage from "$util/CenteredPage.svelte";
	import Inputs from "$lib/Inputs.svelte";

	const onSubmit = console.log;
</script>

<main>
	<CenteredPage>
		<Inputs categories={[
			{
				display: "Basic Metadata",
				properties: [
					{
						id: "appName",

						type: "text",
						label: "App Name:",
						placeholder: "Enter a name for the app..."
					},
					{
						id: "hmm",

						type: "checkbox",
						label: "App Name:",
						placeholder: "Enter a name for the app..."
					}
				]
			}
		]} {onSubmit}></Inputs>
	</CenteredPage>
</main>