<script lang='ts'>
    export let videoID = '';
</script>

<iframe width="560" height="315" 
    src="https://www.youtube-nocookie.com/embed/{videoID}"
    title="YouTube video player"
    frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
/>

<style lang="scss">
    iframe {
        padding: 30px;
    }
</style>