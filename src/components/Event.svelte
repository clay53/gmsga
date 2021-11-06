<script lang="ts">
    import { link } from "svelte-routing";
    export let title: string;
    export let date: string;
    export let color: string;
    export let bg: string;
    export let to: string;
</script>

<a href="{to}" use:link>
    <div style="color: {color}; background-color: {bg}">
        <h1>{title}</h1>
        <p>{date}</p>
    </div>
</a>

<style>
    a {
        display: block;
        max-width: 100vh;
        margin: auto;
    }

    a:hover {
        text-decoration: none;
    }

    div {
        border-radius: 0.5em;
    }

    div h1 {
        margin: 0.5em 0 0.2em 0;
        padding: 0.1em 0 0 0;
    }

    div p {
        margin: 0;
        padding-bottom: 0.5em;
    }
</style>