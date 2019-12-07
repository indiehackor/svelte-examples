<script>
  import Dot from "./Dot.svelte";
  export let ndots = 30;
  export let duration = 2500;

  let dots = [];
  const deg = Math.round(360 / ndots);

  for (var i = 0; i < ndots; i++) {
    dots.push(i);
  }
</script>

<style>
  .dots-container {
    height: 100px;
    display: flex;
    justify-content: center;
  }

  div {
    display: flex;
    justify-content: center;
  }
</style>

<div>
  <span class="dots-container">
    {#each dots as dot, index}
      <Dot {deg} {index} {ndots} {duration} />
    {/each}
  </span>
</div>
