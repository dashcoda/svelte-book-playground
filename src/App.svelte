<script>
  let x = 1;

  $: area = x * x;
  $: volume = x * x * x;
</script>

<div>
  一辺の長さ：
  <button on:click={() => (x = x - 1)} disabled={x <= 1}> - </button>
  {x}m
  <button on:click={() => (x = x + 1)}> + </button>
</div>
<div>面積：{area}m<sup>2</sup></div>
<div>体積：{volume}m<sup>3</sup></div>

<style>
</style>
