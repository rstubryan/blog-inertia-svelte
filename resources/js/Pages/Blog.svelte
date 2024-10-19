<script>
    let count = 0;

    $: double = count * 2;

    function increment() {
        count += 1;
    }

    function decrement() {
        if (count > 0) {
            count -= 1;
        } else {
            count = 0;
        }
    }
</script>

<main>
    <h1>Counter: {count}</h1>
    <h2>Double: {double}</h2>
    <button class="btn btn-primary" on:click={increment}>Increment</button>
    <button on:click={decrement}>Decrement</button>
</main>

<style>
    main {
        text-align: center;
        padding: 1em;
        max-width: 240px;
        margin: 0 auto;
    }

    button {
        margin: 0.5em;
        padding: 0.5em 1em;
        font-size: 1em;
    }
</style>
