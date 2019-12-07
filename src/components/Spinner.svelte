<script>
  import Dot from "./Dot.svelte";
  export let ndots = 30;
  export let duration = 2000;

  let dots = [];
  const deg = Math.round(360 / ndots);

  for (var i = 0; i < ndots; i++) {
    dots.push(i);
  }
</script>

<style>
  .dots-container {
    transform-origin: 53px 3px;
    height: 100px;
    width: 100px;
    position: relative;
    /* animation: rotate 1500ms infinite linear; */
  }

  div {
    display: flex;
    justify-content: center;
    margin-top: 100px;
  }

  @keyframes rotate {
    0%,
    25% {
      transform: rotate(0deg);
    }
    100%,
    75% {
      transform: rotate(-360deg);
    }
  }
</style>

<div>
  <span class="dots-container">
    {#each dots as dot, index}
      <Dot {deg} {index} {ndots} {duration} />
    {/each}
  </span>
</div>
