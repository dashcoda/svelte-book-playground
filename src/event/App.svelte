<script>
  import CustomButton from "./event/CustomButton.svelte";

  function handleClick(event) {
    console.log(event);
    alert(event.detail);
  }
</script>

<CustomButton on:hello={handleClick} />

<style>
</style>
