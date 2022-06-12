<script lang="ts">
    import "../styles/global.scss";
    import Header from "../lib/components/Header.svelte";
    import Footer from "$lib/components/Footer.svelte";
</script>

<Header/>

<slot/>

<Footer/>