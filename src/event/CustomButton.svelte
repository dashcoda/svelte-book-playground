<script>
  import HelloButton from "./HelloButton.svelte";
</script>

<!-- <button on:click>
  <slot />
</button> -->

<HelloButton on:hello>
  <div>ここをクリック</div>
</HelloButton>

<style>
</style>
