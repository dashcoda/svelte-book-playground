<div class="card">
  {#if $$slots.title}
    <div class="title">
      <slot name="title" />
    </div>
  {/if}
  <div class="body">
    <slot />
  </div>
</div>

<style>
  .card {
    border: 1px solid lightgray;
    padding: 1rem;
  }

  .title {
    border-bottom: 1px solid lightgray;
    padding: 0.5em 1rem;
  }

  .body {
    padding: 0.5em 1rem;
  }
</style>
