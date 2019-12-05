<script>
  import { beforeUpdate, afterUpdate } from "svelte";
  export let data;
  export let index;
</script>

<style>
  span {
    background: steelblue;
    margin-right: 15px;
    width: 10px;
    transition: height 200ms ease-out;
  }
</style>

<span style=" height: {5 * data}px; transition-delay: {100 * index}ms;" />
