<script>
    export let title;
    export let monthYearStart;
    export let monthYearEnd;
    export let description;
</script>

<div class="titleRow">
    <span class="title">{title}</span>
    <span>{monthYearStart}</span>
    {#if monthYearEnd}
        <span>&nbsp-&nbsp</span>
    {/if}
    <span>{monthYearEnd}</span>
</div>
<p>{description}</p>

<style>
    .titleRow {
        display: flex;
        align-items: stretch;
        width: 70%;
        margin: auto;
    }
    span {
        font-family: Arial, Helvetica, sans-serif;
    }
    span.title {
        font-weight: bold;
        padding-right: 1em;
    }
    p {
        margin: auto;
        font-family: 'Courier New', Courier, monospace;
        width: 70%;
        padding: 1em;
    }
</style>