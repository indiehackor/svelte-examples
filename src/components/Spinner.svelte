<script>
  export let ndots = 20;
  export let duration = 2000;
  import Dot from "./Dot.svelte";
  let dots = [];
  const deg = Math.round(360 / ndots);

  for (var i = 0; i < ndots; i++) {
    dots.push(i);
  }
</script>

<style>
  .dots-container {
    height: 100px;
    margin-top: 100px;
    position: relative;
  }
</style>

<div class="dots-container">
  {#each dots as dot, index}
    <Dot {deg} {index} {ndots} {duration} />
  {/each}
</div>
