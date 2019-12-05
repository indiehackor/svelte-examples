<script>
  import Column from "./Column.svelte";
  let data = [20, 40, 50, 30, 60, 70, 30, 90, 50, 80];

  const getRandom = () => Math.floor(Math.random() * 100);

  const randomize = () => {
    data = data.map(() => getRandom());
  };
</script>

<style>
  .graph {
    display: flex;
    margin: 0 auto;
    height: 500px;
    align-items: flex-end;
  }
</style>

<div class="graph-container">
  <button on:click={randomize}>RANDOMIZE</button>
  <div class="graph">
    {#each data as value, i}
      <Column data={value} index={i} />
    {/each}
  </div>
</div>
