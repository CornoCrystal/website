<script lang="ts">
    import { VITE_BACKEND_URL } from "$lib/env";
import { invalid_attribute_name_character } from "svelte/internal";

    console.log(VITE_BACKEND_URL);

    async function getChangelog () {
		var res = await fetch('https://' + VITE_BACKEND_URL + '/changelog');
        const data = await res.json();

        if (res.ok) {
            return data;
        } else {
            throw new Error(data);
        }
	}
</script>

<div class="main">
    {#await getChangelog()}
        <p>Loading...</p>
    {:then changelog}
        {#each changelog as change}
            <div class="change">
                <img class="avatar" src="{change.author.avatar}" alt="{change.author.name}">
                <h1>{change.author.name}</h1>
                <h2>{change.date}</h2>
                <p>{@html change.content}</p>
                {#each change.attachments as attachment}
                    <!-- svelte-ignore a11y-missing-attribute -->
                    <img src="{attachment}"/>
                {/each}
            </div>
        {/each}
    {:catch error}
    <p style="color: red">{error.message}</p>
    {/await}
</div>

<style lang="scss">
    @import "../styles/global.scss";
    h1 {
        color: $color-3;
        text-shadow: 0 0 5px $color-3;
    }

    .main {
        text-align: center;
    }

    :global(strong) {
        color: white;
        font-weight: 400;
    }

    .change {
        padding: 50px;
    }

    .avatar {
        width: 100px;
    }

    img {
        box-shadow: 0 0 15px $color-3;
    }
</style>