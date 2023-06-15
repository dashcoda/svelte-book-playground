<script>
  import Button from "../Button.svelte";
  import Box from "../Box.svelte";
  import Card from "../Card.svelte";
  import List from "../List.svelte";

  const props = { label: "ボタン", disabled: true };
  const user1 = {
    firstName: "sean",
    id: "2378467",
    bio: "this is bio",
  };
</script>

<Box>
  <!-- <Button {...props} user={user1} />
  <h3>Svelteについて</h3>
  <p>SvelteはこれまでにないUIフレームワークです。</p> -->
</Box>

<Card>
  <!-- <h3 slot="title">Svelteについて</h3> -->
  <p>SvelteはこれまでにないUIフレームワークです。</p>
</Card>

<List>
  <span class="item" slot="item" let:item>{item}</span>
</List>

<style>
  .item {
    color: blue;
  }
</style>
