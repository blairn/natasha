<script>
    import MoveableBox from "../components/MoveableBox.svelte";
</script>

<style>
	@media (min-width: 480px) {
		h1 {
			font-size: 4em;
		}
	}
</style>

<svelte:head>
	<title>Sapper project template</title>
	<link href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet" integrity="sha384-wvfXpqpZZVQGK6TAh5PVlGOfQNHSoD2xbE+QkPxCAFlNEevoEH3Sl0sibVcOQVnN" crossorigin="anonymous">
</svelte:head>

<h1>Great success!</h1>
<MoveableBox></MoveableBox>

<p><strong>Try editing this awesome file (src/routes/index.svelte) to test live reloading.</strong></p>
