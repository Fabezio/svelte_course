<script>
	import Text from './Text.svelte'
	import Button from './Button.svelte'
	import Divider from './Divider.svelte'
	import GC from './GaussConter.svelte'
	export let name
	export let src
	$: {if (name=="fabezio") console.log('wow')
	else console.log(`hello ${name}`)}
</script>

<main>
	<h1>Salut {name = 'Tout le monde'}!</h1>
	<img style="width: 100px;" src='{src}' alt='my img'>
	<p>Consultez le  <a href="https://svelte.dev/tutorial">tuto Svelte</a> pour apprendre à créer des applications Svelte.</p>
	<Divider/>
	<Text/>
	<Divider/>
	<Button/>
	<Divider/>
	<GC/>
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