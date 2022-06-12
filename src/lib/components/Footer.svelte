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
        padding: 10px;
        text-align: center;
        bottom: 0;
        position: absolute;
        width: 100%;
        margin-top: auto;
        height: $height;
        background-color: $color-2;

        p {
            color: gray;
        }
    }
</style>