<script>
    import { getContext } from "svelte";

    const userName = getContext('username-context')
</script>

<h2>Component F</h2>
<h2>Username - {userName}</h2>