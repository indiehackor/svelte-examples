<script>
  import Graph from "./components/Graph.svelte";
  import Spinner from "./components/Spinner.svelte";
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }
</style>

<main>
  <h1>Loader</h1>
  <Spinner ndots={20} />
  <h1>Graph</h1>
  <Graph />
</main>
