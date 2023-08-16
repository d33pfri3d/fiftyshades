<script>
  import CopyButton from "./lib/CopyButton.svelte";
  import MadeBy from "./lib/MadeBy.svelte";
  import { grays } from "./lib/grays";

  console.log(
    "Thanks to this tweet - https://twitter.com/WebbingTheRock/status/566311952847499264/photo/1"
  );

</script>

<main>
  <header>
    <h1>{grays.length} Shades of Gray</h1>
    <MadeBy />
  </header>

  <div class="grays">
    {#each grays as gray}
      <div class="box">
        <div class="gray" style="background-color: {gray.hex}" />

        <div class="info">
          <p>Hex: {gray.hex}</p>

          <CopyButton text={gray.hex} />
        </div>
      </div>
    {/each}
  </div>
</main>

<style>
  header {
    display: flex;
    flex-direction: column-reverse;
    margin-bottom: 1rem;
  } 

  .box {
    display: flex;
    flex-direction: column;
    height: 200px;
    width: 100%;
    background-color: beige;
    padding: 5px;
    gap: 1rem;
  }

  .info {
    color: black;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    justify-content: space-between;
  }

  .grays {
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    gap: 1rem;
    justify-content: space-around;
  }

  .gray {
    height: 100px;
    width: 100%;
  }

  p {
    margin: 0;
    font-size: 0.8rem;
    font-family: monospace;
  }

  @media screen and (min-width: 768px) {

    header {
      flex-direction: row;
      align-items: center;
      justify-content: space-between;
    }
    .grays {
      flex-direction: row;
    }

    .box, .gray {
      width: 100px;
    }
}
</style>
