<script>
  import { CopyButton } from "./lib/CopyButton.svelte";

  console.log(
    "Thanks to this tweet - https://twitter.com/WebbingTheRock/status/566311952847499264/photo/1"
  );

  const grays = [
    { hex: "#A0A0A0" },
    { hex: "#9E9E9E" },
    { hex: "#9B9B9B" },
    { hex: "#9A9A9A" },
    { hex: "#9B9A9A" },
    { hex: "#989797" },
    { hex: "#949393" },
    { hex: "#908F8F" },
    { hex: "#8D8C8C" },
    { hex: "#8A8989" },
    { hex: "#888787" },
    { hex: "#848383" },
    { hex: "#807E7E" },
    { hex: "#7C7A7A" },
    { hex: "#797878" },
    { hex: "#757474" },
    { hex: "#717070" },
    { hex: "#727272" },
    { hex: "#6E6E6E" },
    { hex: "#6B6969" },
    { hex: "#696868" },
    { hex: "#676666" },
    { hex: "#646363" },
    { hex: "#626161" },
    { hex: "#5F5F5F" },
    { hex: "#5D5D5D" },
    { hex: "#5A5A5A" },
    { hex: "#565656" },
    { hex: "#535353" },
    { hex: "#535453" },
    { hex: "#505150" },
    { hex: "#4D4E4D" },
    { hex: "#4A4A4A" },
    { hex: "#474747" },
    { hex: "#434343" },
    { hex: "#404040" },
    { hex: "#3D3D3D" },
    { hex: "#3A3A3A" },
    { hex: "#383838" },
    { hex: "#353535" },
    { hex: "#323232" },
    { hex: "#2A2B2B" },
    { hex: "#2D2B2B" },
    { hex: "#2C2B2B" },
    { hex: "#292828" },
    { hex: "#272626" },
    { hex: "#242323" },
    { hex: "#202020" },
    { hex: "#2F2F2F" },
    { hex: "#1E1E1E" },
  ];
</script>

<main>
  <h1>50 Shades of Gray</h1>

  <!-- Map over the grays and generate a box -->

  <div class="grays">
    {#each grays as gray}
      <div class="box">
        <div class="gray" style="background-color: {gray.hex}" />

        <div class="info">
          <p>{gray.hex}</p>
        </div>
      </div>
    {/each}
  </div>
</main>

<style>
  .box {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 100px;
    width: 100px;
    background-color: beige;
    padding: 5px;
  }

  .info {
    color: black;
  }

  .grays {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 1rem;
  }

  .gray {
    height: 100px;
    width: 100px;
  }
</style>
