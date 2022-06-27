<script>
    import { onMount } from "svelte";
    let downloadDir = ""

    function handleInput(event) {
        console.log(event)
    }

    onMount(async () => {
        downloadDir = await (await fetch("./dldir")).text()
    })
</script>

<!-- <input 
    type="file" 
    name="Download folder" 
    id="dl-folder-input"
    webkitdirectory 
    directory 
    multiple="false" 
    on:input={handleInput}
/> -->
<div    >Currently will download to: <strong>{downloadDir}</strong></div>

<style>
    div {
        margin: .5rem 0;
    }
</style>