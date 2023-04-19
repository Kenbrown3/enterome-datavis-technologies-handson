<script>
  let current = "";
</script>

<!-- We will cover buttons later on! -->
<button
  class={current === "messi" ? "selected btn" : "btn btn-secondary"}
  on:click={() => (current = "messi")}
>
  Messi
</button>

<button
  class={current === "ronaldo" ? "selected btn" : "btn btn-secondary"}
  on:click={() => (current = "ronaldo")}
>
  Ronaldo
</button>

<button
  class={current === "neymar" ? "selected btn" : "btn btn-secondary"}
  on:click={() => (current = "neymar")}
>
  Neymar
</button>

<style>
  .selected {
    background-color: rgb(49, 72, 164);
  }
</style>
