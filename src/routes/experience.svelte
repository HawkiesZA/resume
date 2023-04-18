<script>
    export let title;
    export let monthYearStart;
    export let monthYearEnd;
    export let description;
</script>

<div class="card">
    <div class="titleRow">
        <span class="title">{title}</span>
        <span>{monthYearStart}</span>
        {#if monthYearEnd}
            <span>&nbsp-&nbsp</span>
        {/if}
        <span>{monthYearEnd}</span>
    </div>
    <p>{description}</p>
</div>

<style>
    .card {
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
        transition: 0.3s;
        padding: 0.5em;
        margin-bottom: 1em;
    }
    .card:hover, .card:focus {
        background-color: #f5f5f5;
    }
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