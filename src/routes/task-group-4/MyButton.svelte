<script>
    export let click_event = () => alert("testing");
    export let text = "Send"
</script>

<button on:click={click_event}>
    {text}
</button>
