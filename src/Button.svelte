<script>
    export let label = ''
    export let user;
    export let disabled = false
</script>

<button {disabled}>{label}</button>
<h2>{user.firstName}(id: {user.id})</h2>
<p>{user.bio}</p>

<style></style>