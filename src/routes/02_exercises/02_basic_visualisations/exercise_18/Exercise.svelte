<!doctype html />
<html lang="en">
  <head>
    <!--Step 2-->
    <script src="https://d3js.org/d3.v4.min.js"></script>
  </head>
  <body>
    <!--Step 2-->
    <svg width="500" height="400" />
    <script>
      // Step 1
      var dataset1 = [
        [4, 2],
        [16, 4],
        [36, 6],
        [49, 7],
        [81, 9],
      ];

      // Step 3
      var svg = d3.select("svg"),
        margin = 200,
        width = svg.attr("width") - margin, //300
        height = svg.attr("height") - margin; //200

      // Step 4
      var xScale = d3.scaleLog().domain([0.1, 100]).range([0, width]),
        yScale = d3.scaleLinear().domain([2, 9]).range([height, 0]);

      var g = svg
        .append("g")
        .attr("transform", "translate(" + 100 + "," + 100 + ")");

      // Step 5
      // Title
      svg
        .append("text")
        .attr("x", width / 2 + 100)
        .attr("y", 100)
        .attr("text-anchor", "middle")
        .style("font-family", "Helvetica")
        .style("font-size", 20)
        .text("Scatter Plot");

      // X label
      svg
        .append("text")
        .attr("x", width / 2 + 100)
        .attr("y", height - 15 + 150)
        .attr("text-anchor", "middle")
        .style("font-family", "Helvetica")
        .style("font-size", 12)
        .text("Independant");

      // Y label
      svg
        .append("text")
        .attr("text-anchor", "middle")
        .attr("transform", "translate(60," + height + ")rotate(-90)")
        .style("font-family", "Helvetica")
        .style("font-size", 12)
        .text("Dependant");

      // Step 6
      g.append("g")
        .attr("transform", "translate(0," + height + ")")
        .call(d3.axisBottom(xScale));

      g.append("g").call(d3.axisLeft(yScale));

      // Step 7
      svg
        .append("g")
        .selectAll("dot")
        .data(dataset1)
        .enter()
        .append("circle")
        .attr("cx", function (d) {
          return xScale(d[0]);
        })
        .attr("cy", function (d) {
          return yScale(d[1]);
        })
        .attr("r", 2)
        .attr("transform", "translate(" + 100 + "," + 100 + ")")
        .style("fill", "#CC0000");
    </script>
  </body>
</html>
