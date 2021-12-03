<script>
	export let name;
	let count = 0;
	$: doubled = count * 2;

function incrementCount() {
	count++;
	console.log(`teller trykket på ${count}`);
}
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Tester litt funksjonalitet</p>
	<button on:click={incrementCount}>
	Klikket på tellerknappen {count} {count ===1 ? 'gang' : 'ganger'}</button>	

	<p>{count} doblet er {doubled}</p>
	
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

						

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>