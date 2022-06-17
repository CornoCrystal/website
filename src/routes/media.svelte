<script lang="ts">
    import Youtube from "$lib/components/Youtube.svelte";

    let videos = [
        "DCdKl_VziGQ",
        "w_ulE7kSDzE",
        "azSt2a761gw",
        "zw9ISMN2G10",
        "GR893Wftu5M",
        "4hybIemF33U",
        "Ayg4PXwV5sY"
    ]
</script>

<div class="videos">
    {#each videos as video}
        <Youtube videoID={video}/>
    {/each}
</div>

<style lang="scss">
    .videos {
        display: inline-block;
    }
</style>