<script lang="ts">
    import Navbar from "./Navbar.svelte";
</script>

<footer>
    <p>Desenvolvido por Maizena.</p>
    <Navbar items=
        {
            [
                {
                    link: "https://github.com/CornoCrystal/website",
                    name: "Código Fonte",
                    target: "__blank"
                },
                {
                    link: "https://github.com/CornoCrystal/",
                    name: "GitHub",
                    target: "__blank"
                },
            ]
        }
    />
</footer>

<style lang="scss">
    @import '../../styles/vars.scss';

    footer {
        text-align: center;
        margin-top: auto;
        padding: 10px;
        bottom: 0;
        background-color: $color-2;
    }
</style>