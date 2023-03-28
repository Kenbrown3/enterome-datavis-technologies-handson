<script>
  let clicked = false;
</script>

<div>
  <button class="btn btn-primary" on:click={() => (clicked = true)}>
    click here
  </button>
  <!--  -->
  {#if !clicked}
    You need to click the button
  {:else}
    You clicked the button
  {/if}
</div>
