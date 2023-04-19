<script>
  // Dimensions
  import { scaleLog } from "d3-scale";
  const scale = scaleLog().domain([2, 9]).range([0, 100]);
  const width = 800;
  const height = 100;
  const margin = { top: 5, right: 5, bottom: 5, left: 5 };
  const innerWidth = width - margin.left - margin.right;
  const innerHeight = height - margin.top - margin.bottom;

  // Array
  const values = [2, 4, 6, 7, 9];
</script>

{#each values as value}
  <svg viewBox="0 0 {width} {height}">
    <g transform="translate({margin.left},{margin.top})">
      <circle cx={scale(value)} cy={value} r="10" />
    </g>
  </svg>
{/each}
