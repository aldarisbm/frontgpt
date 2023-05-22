<script>
	import Counter from './Counter.svelte';
</script>

<svelte:head>
	<title>joseberr.io</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>
		Welcome
	</h1>
	<Counter />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}

	h1 {
		width: 100%;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
