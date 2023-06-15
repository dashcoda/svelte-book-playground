<script>
  let array = ["Svelte", "React", "Vue", "Angular"];
</script>

{#each array as item}
  <slot name="item" {item} />
{/each}

<style>
</style>
