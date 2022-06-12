<script lang="ts">
    export let items: any[] = [];
</script>

<navbar>
    {#each items as item}
        <a href="{item.link}" target="{item.target}" class="nav-link">
            <span>{item.name}</span>
        </a>
    {/each}
</navbar>

<style lang="scss">
    @import '../../styles/vars.scss';

    :global(a) {
        text-decoration: none;
        align-items: center;
        font-size: large;
        display: inline-block;
        color: white;
        padding: 10px;
        transition: 0.1s ease-in-out;
    }

    :global(a:hover) {
        color: $tertiary-purple;
        text-shadow: 0 0 5px $tertiary-purple;
    }
</style>