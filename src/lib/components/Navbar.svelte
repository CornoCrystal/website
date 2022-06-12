<script lang="ts">

    export let items: any[] = [];

</script>

<navbar>
    {#each items as item}
        <a href="{item.link}" class="nav-link">
            <span>{item.name}</span>
        </a>
    {/each}
</navbar>