<script>
	import Chat from './Chat.svelte';
</script>

<svelte:head>
	<title>joseberr.io</title>
	<meta name="description" content="Jose Berrio" />
</svelte:head>

<section>
	<h1>
		Welcome
	</h1>
	<Chat />
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

</style>
