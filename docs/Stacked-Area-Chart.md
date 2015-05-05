---
title: StackedArea Chart
anchor: stacked-area-chart
---

### Introduction
A stacked area chart is a line chart extension that is optimized for stacked data.

<div class="canvas-holder">
	<canvas width="250" height="125"></canvas>
</div>

### Example usage
```javascript
var myStackedAreaChart = new Chart(ctx).StackedArea(data, options);
```

### Data structure

```javascript
var data = {
	labels: ["January", "February", "March", "April", "May", "June", "July"],
	datasets: [
		{
			label: "My First dataset",
			fillColor: "rgba(220,220,220,0.5)",
			strokeColor: "rgba(220,220,220,0.8)",
			highlightFill: "rgba(220,220,220,0.75)",
			highlightStroke: "rgba(220,220,220,1)",
			data: [65, 59, 80, 81, 56, 55, 40]
		},
		{
			label: "My Second dataset",
			fillColor: "rgba(151,187,205,0.5)",
			strokeColor: "rgba(151,187,205,0.8)",
			highlightFill: "rgba(151,187,205,0.75)",
			highlightStroke: "rgba(151,187,205,1)",
			data: [28, 48, 40, 19, 86, 27, 90]
		}
	]
};
```

### Chart Options

These are the customisation options specific to StackedArea charts. These options are merged with the [global chart configuration options](#getting-started-global-chart-configuration), and form the options of the standard line chart.

```javascript
{
	//Boolean - Whether points should be rendered on a percentage base
	relativePoints : false,
}
```

You can override these for your `Chart` instance by passing a second argument into the `StackedArea` method as an object with the keys you want to override.

For example, we could have a stacked point chart without a stroke on each point by doing the following:

```javascript
new Chart(ctx).StackedArea(data, {
	relativePoints: true
});
// This will create a chart with all of the default options, merged from the global config,
//  and the StackedArea chart defaults but this particular instance will have `relativePoints` set to true.
```