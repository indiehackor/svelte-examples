<script>
  export let index;
  export let deg;
  export let ndots;
  export let duration;
  export let radius = 50;
  export let shiftRadius = 60;
</script>

<style>
  .dot {
    height: 6px;
    width: 6px;
    border-radius: 3px;
    background: salmon;
    position: absolute;
    animation: slide var(--ndots) ease-in-out var(--delay) infinite;
  }

  @keyframes slide {
    0%,
    16% {
      transform: rotate(var(--deg)) translateX(var(--radius));
    }
    8% {
      transform: rotate(var(--deg)) translateX(var(--shiftRadius));
    }
  }
</style>

<span
  class="dot"
  style="--shiftRadius: {shiftRadius}px; --radius: {radius}px; --deg: {index * deg}deg;
  --delay: {index * (duration / ndots)}ms; --ndots: {ndots * (duration / ndots)}ms;
  transform: rotate(var(--deg)) translateX({radius - 3}px)" />
