<script>
  let rand = -1;

  async function getRand() {
    rand = await (await fetch("./rand")).text()
  }
</script>

<h1>Your number is {rand}!</h1>
<button on:click={getRand}>Get a random number</button>