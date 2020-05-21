<script>
let nb= [1, 2, 3]
nb.bar = 'baz'
function addNumber () {
  nb = [...nb, nb.length + 1]
}
$: sum = nb.reduce((t, n) => t+n , 0)
</script>

<p style="width: 50%; margin: 0 auto 10px">{nb.join(' + ')} = {sum}</p>
<button on:click={addNumber} style="background: cyan; padding: 0.5em 1em; border-radius: .5em">Ajouter nombre suivant</button>