<script>
  export let index;
  export let deg;
  export let ndots;
  export let duration;
  export let radius = 50;
  export let shiftRadius = 30;
</script>

<style>
  .dot {
    height: 8px;
    width: 8px;
    border-radius: 4px;
    margin-left: 5px;
    background: darkslategrey;
    animation: slide var(--ndots) ease-out var(--delay) infinite;
  }

  @keyframes slide {
    0%,
    16% {
      transform: translateY(var(--radius));
    }
    8% {
      transform: translateY(var(--shiftRadius));
    }
  }
</style>

<div
  class="dot"
  style="--shiftRadius: {shiftRadius}px; --radius: {radius}px; --deg: {index * deg}deg;
  --delay: {index * (duration / ndots)}ms; --ndots: {ndots * (duration / ndots)}ms;
  transform: translateY({radius}px)" />
