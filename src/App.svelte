<script>
import Button from "./Button.svelte";

const label = 'ボタン'
const user1 = {
  firstName: 'sean',
  id: '2378467',
  bio: 'this is bio'
}
</script>

<Button disabled {label} user = {user1}/>

<style>

</style>