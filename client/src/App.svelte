<script>
  import DestPicker from './components/DestPicker.svelte'

  let rand = -1;

  async function getRand() {
    rand = await (await fetch("./rand")).text()
  }
</script>

<h1> youtube song downloader</h1>
<DestPicker/>
<button on:click={getRand}>Get a random number</button>