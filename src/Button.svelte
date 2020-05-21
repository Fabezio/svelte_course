<script>
let count =  0
function handleClick() {
  count += 1
}
</script>
<button on:click={handleClick}>Cliquez ici pour incrémenter de 1</button>
<p>{count}</p>
{#if count >= 10}
<p style="color: orange">Faites chauffer le bouton!</p>
{:else if count > 0}
<p style="color: blue">Bien joué!</p>
{/if}