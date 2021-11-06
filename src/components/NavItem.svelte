<script lang="ts">
    import { link } from "svelte-routing";
    export let to: string;
</script>

<a href="{to}" use:link><slot/></a>

<style>
    a {
        background-color: maroon;
        padding: 0.2em 0.5em;
        margin: 0 0.1em;
        color: white;
        font-size: 1.5em;
        border-radius: 0.25em;
    }
</style>