<script>
let count =  0
function handleClick() {
  count += 1
}
</script>
<button on:click={handleClick}>click here to add 1</button>
<p>{count}</p>
{#if count >= 10}
<p style="color: orange">burn your button!</p>
{:else if count > 0}
<p style="color: blue">well done!</p>
{/if}