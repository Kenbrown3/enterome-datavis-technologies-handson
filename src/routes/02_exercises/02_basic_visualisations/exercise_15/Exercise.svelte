<script>
  const width = 100;
  const height = 100;
  const margin = { top: 5, right: 5, bottom: 5, left: 5 };
  const innerWidth = width - margin.left - margin.right;
  const innerHeight = height - margin.top - margin.bottom;
</script>

<svg {width} {height}>
  <g transform="translate({margin.left}, {margin.top})">
    <rect
      x={width / 4}
      y={height / 4}
      width="40"
      height="40"
      style="fill:yellow"
    />
    <circle cx={width - 20} cy={height - 20} r="20" style="fill:skyblue" />
  </g>
</svg>

<style>
  svg {
    border: 1px solid rgb(0, 0, 0);
    border-radius: 5px;
  }
</style>
