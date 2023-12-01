<script>
    import { writable } from "svelte/store";
    let counter = writable(0);

    $:messageinabottle = buildMessage($counter);

    function buildMessage(num) {
        return "the amount of displayed " + num + " times";
    }

</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<div>
    <button on:click={() => counter.update(a=>a++)}>Add</button>
</div>

<div>
    {messageinabottle}
</div>