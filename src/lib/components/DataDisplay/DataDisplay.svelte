<script>
    import Chart from "./Chart.svelte";

    const names = [
        "annual_uploads",
        "cumulative_uploads",
        "views",
        "location_created",
        "saves",
        "duration",
        "likes",
        "comments",
        "category",
        //"music",
        //"live_status"
    ];

</script>



<div class="charts-wrapper">
    {#each names as name (name)}
        <div class="canvas-wrap">
            <Chart {name}></Chart>
        </div>
    {/each}
</div>


<style>
    .charts-wrapper {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        overflow-y: scroll;
    }

    .canvas-wrap {
        flex: 1 1 50%;
        position: relative;
        aspect-ratio: 16 / 9;
        min-width: 800px;
        padding: 1rem;
    }

    canvas{
        padding: 1rem;
    }
</style>