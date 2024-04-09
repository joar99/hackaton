<template>
  <div id="simple-chart"></div>
</template>

<script setup>
import { onMounted } from 'vue';
import Highcharts from 'highcharts';

// Component setup
onMounted(() => {
  // Chart configuration
  const chartOptions = {
    chart: {
      type: 'bar', // Change chart type as needed
      renderTo: 'simple-chart'
    },
    title: {
      text: 'Fruit Consumption'
    },
    xAxis: {
      categories: ['Apples', 'Bananas', 'Oranges']
    },
    yAxis: {
      title: {
        text: 'Fruit eaten'
      }
    },
    series: [{
      name: 'Jane',
      data: [1, 0, 4]
    }, {
      name: 'John',
      data: [5, 7, 3]
    }]
  };

  // Initialize chart
  Highcharts.chart(chartOptions);
});
</script>

<style>
/* Style your chart container as needed */
#simple-chart {
  width: 100%;
  height: 400px;
}
</style>


