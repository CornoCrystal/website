<script lang="ts">
    import Navbar from "./Navbar.svelte";
</script>

<header>
    <a href="/"><img src="./logo.png" alt="logo do corno crystal"></a>
    <Navbar items=
        {
            [
                {
                    link: "/media",
                    name: "Media",
                },
                {
                    link: "/anuncios",
                    name: "Anúncios",
                },
                {
                    link: "/donate",
                    name: "Donate",
                },
            ]
        }
    />
</header>

<style lang="scss">
    @import '../../styles/global.scss';

    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0 100px;
        max-height: $height;
        background-color: $color-2;
        //border-bottom: 5px solid $primary-purple;

        img {
            max-height: $height * 2;
        }
    }
</style>